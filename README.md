## Clean Coder (uncle BoB)


---

**Table of contents:**

- [What is this?](#what-is-this)
- [Clean Code](#clean-code)
- [Names](#names)
- [Function](#function)
- [Function Structure](#function-structure)
  * [Arguments](#arguments)


---

## What is this?

Hello 👋

this repository is a summary of the collection of robert c martin books
and python examples to make it more understandably 
(clean code, clean coder , clean architect, clean agile)

**Few important notes about it:**

1. It's derived from many years of experience & many Django projects, both big & small.
2. It's pragmatic. All things mentioned here are things tested in production.
3. It's opinionated. This is how we build applications with Django.

**SomeThing important that I forgot**


## Clean Code


## Names
1. chose your name thoughtfully
2. communicate your INTENT
3. avoid disinformation
4. pronounceable names
5. avoid encoding (like adding s,i,b,l, etc. to sow that variable is list string or anytype)
6. choose your name so that code can be read like a well-written latter
7. class and variables name should be named, functions should be verse, and boolean should be (is_user_admin)
8. follow the scope rule
    - variables in big scope should have a descriptive big name, in small scope should have a short name
    - functions in long scope should have a short name, in small scopes should have a large descriptive name



## Function
1. do 1 thing
2. do it well
3. do it only
4. it should be small even smaller than that
5. 4-6 line
6. small descriptive name
7. extract till you drp
**Before**
```python
def add_user(user_info: dict, current_user: User):
    created_by = str(current_user.id)
    new_user = User(**user_info)
    new_user.created_by = created_by
    new_user.created_date = datetime.utcnow()
    new_user.password = mongodb_utils.make_password(user_info.get('password', None))
    new_user.parents += current_user.parents
    new_user.parents.append(created_by)
    new_user.save()
    current_user.children.append(str(new_user.id))
    current_user.save()
    if current_user.parents:
        p_users = find_users_by_ids(current_user.parents, need_deleted_users=True)
        for p_user in p_users:
            p_user.children.append(str(new_user.id))
            p_user.save()
    return new_user.id
```
**After**
```python
class CreateUser:
    def __init__(self, input_user: UserIn, current_user: User):
        self.input_user = input_user
        self.new_user: User = User(**jsonable_encoder(input_user))
        self.current_user: User = current_user

    def add_user(self):
        self.__annotate_new_user_meta_data()
        self.new_user.save()
        self.__add_children_user_id_to_parents_users()
        return self.new_user.id

    def __annotate_new_user_meta_data(self):
        self.new_user.created_date = datetime.utcnow()
        self.new_user.password = mongodb_utils.get_password_hash(self.input_user.password)
        self.__add_parents_users_id_to_new_user()

    def __add_parents_users_id_to_new_user(self):
        created_by = str(self.current_user.id)
        self.new_user.created_by = created_by
        self.new_user.parents += self.current_user.parents
        self.new_user.parents.append(created_by)

    def __add_children_user_id_to_parents_users(self):
        self.current_user.children.append(str(self.new_user.id))
        self.current_user.save()
        if self.current_user.parents:
            self.__add_children_user_id_to_current_user_parents()

    def __add_children_user_id_to_current_user_parents(self):
        p_users = find_users_by_ids(self.current_user.parents, need_deleted_users=True)
        for p_user in p_users:
            p_user.children.append(str(self.new_user.id))
            p_user.save()
```

## Function Structure

### Arguments
1. **3** arguments **MAX**
    - if 3 or more arguments are so needed to pass together, why aren't they an object
2. same as constructor in class
    - better to use nicely named setter functions over a constructor with a hole bunch of arguments
3. no boolean arguments ever
    - if a function does two things, it's two functions
4. innes not outies
   - never use output as an argument, arguments should go into the function not coming out

```python
result = []
def add_data_to_list(arg: any, result:  list()):
    result.append(arg)
print(result)
```


5. the null defence
   - passing a null to a function or writing a function that expect a null to be passed in
   - is almost as bas as passing a boolian into the function
   - actually it's worse cuz it's not abuse taht it's two possible state 
   - write two function one that take null an onother that don't
   - don't use null as a sudo boolian
   
6. the step-down rule
    - public up - private down _ up importance—down detail
7. it's better to do a suboptimal convention that confuses every body


### Switch Case
