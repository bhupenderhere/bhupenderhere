```python
from typing import Tuple
from dataclasses import dataclass


class Meta(type):
    def __new__(cls, name, bases, attrs):
        new_cls = super().__new__(cls, name, bases, attrs)
        return dataclass(unsafe_hash=True, frozen=True)(new_cls)


class Bio(metaclass=Meta):
    name        : str = "Bhupender"
    designation : str = "Software Engineer"
    company     : str = "Zenarate"
    base        : str = "Gurugram, Haryana"
    dob         : str = "15 December, 2001"
    nationality : str = "Indian"


class Stack(metaclass=Meta):
    frontend    : Tuple[str, ...] = ("HTML", "CSS", "JavaScript", "ReactJS", "Boostrap", "TailWind", "MaterialUI")
    backend     : Tuple[str, ...] = ("Python", "Flask", "FastAPI", "NodeJS")
    database    : Tuple[str, ...] = ("MySQL", "SQLite3", "MongoDB", "Firebase")
    datascience : Tuple[str, ...] = ("Pandas", "Numpy", "Matplotlib", "Scikit Learn")
    office      : Tuple[str, ...] = ("MS Word", "MS PowerPoint", "MS Excel")
    tools       : Tuple[str, ...] = ("GIT", "GitHub", "GitLab", "JIRA", "Postman", "VS Code", "Docker")
    aws         : Tuple[str, ...] = ("Glue", "AppSync", "SageMaker", "S3", "Athena", "Lambda", "RDS", "Cloudwatch")
    ongoing     : Tuple[str, ...] = ("Prompt Engineering", "NLP", "Vector DB")


class Social(metaclass=Meta):
    github      : str = "https://github.com/bhupenderhere"
    instagram   : str = "https://instagram.com/bhupenderhere"
    twitter     : str = "https://twitter.com/bhupenderhere"
    linkedin    : str = "https://linkedin.com/in/bhupenderhere/"
    mail        : str = "bhupender.contact@gmail.com"
```
