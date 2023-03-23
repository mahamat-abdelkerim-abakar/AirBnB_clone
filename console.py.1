#!/usr/bin/python3
# -*- coding: utf-8 -*-
"""Console Module
This module controls all databases.
Can create, modify and delete instances.
"""

import cmd
from datetime import datetime
import models
from models.amenity import Amenity
from models.base_model import BaseModel
from models.city import City
from models.place import Place
from models.review import Review
from models.state import State
from models.user import User
import shlex  # for splitting the line along spaces except in double quotes


class_personalize = {"Amenity": Amenity, "BaseModel": BaseModel, "City": City,
                     "Place": Place, "Review": Review, "State": State,
                     "User": User}


class HBNBCommand(cmd.Cmd):
    """Command processor class."""
    prompt = '(hbnb) '

    def do_quit(self, line):
        """Quit command to exit the program.
        """
        return True

    def do_EOF(self, line):
        """Quit command to exit the program.
        """
        return True

    def emptyline(self):
        """
        When an empty line is entered in response to the prompt,
        it won't repeat the last nonempty command entered.
        """
        pass

    def do_create(self, line):
        """Creates a new instance of a class"""
        args = shlex.split(line)
        """Split the passed arguments to interpret
        them as console commands and store them in an array
        """
        if len(args) == 0:
            print("** class name missing **")
            return False
        if args[0] in class_personalize:
            instance = class_personalize[args[0]]()
            print(instance.id)
            instance.save()
        else:
            print("** class doesn't exist **")
            return False

    def do_show(self, arg):
        """Prints an instance as a string based on the class and id"""
        args = shlex.split(arg)
        if len(args) == 0:
            print("** class name missing **")
            return False
        if args[0] in class_personalize:
            if len(args) > 1:
                key = args[0] + "." + args[1]
                """
                In this case if two arguments are passed, concatenate
                with dot to be able to execute the action, eg: show
                User, it will execute User.show to display user data.
                """
                if key in models.storage.all():
                    print(models.storage.all()[key])
                else:
                    print("** no instance found **")
            else:
                print("** instance id missing **")
        else:
            print("** class doesn't exist **")

    def do_destroy(self, arg):
        """Deletes an instance based on the class and id"""
        args = shlex.split(arg)
        if len(args) == 0:
            print("** class name missing **")
        elif args[0] in class_personalize:
            if len(args) > 1:
                key = args[0] + "." + args[1]
                if key in models.storage.all():
                    models.storage.all().pop(key)
                    models.storage.save()
                else:
                    print("** no instance found **")
            else:
                print("** instance id missing **")
        else:
            print("** class doesn't exist **")

    def do_all(self, arg):
        """Prints string representations of instances"""
        args = shlex.split(arg)
        obj_list = []
        if len(args) == 0:
            for value in models.storage.all().values():
                obj_list.append(str(value))
            print("[", end="")
            print(", ".join(obj_list), end="")
            print("]")
            """
            We use these characters to divide the impression
            of each instance when showing them all
            """
        elif args[0] in class_personalize:
            for key in models.storage.all():
                if args[0] in key:
                    obj_list.append(str(models.storage.all()[key]))
            print("[", end="")
            print(", ".join(obj_list), end="")
            print("]")
        else:
            print("** class doesn't exist **")

    def do_update(self, arg):
        """Update an instance based on the class name, id, attribute & value"""
        args = shlex.split(arg)
        integers = ["number_rooms", "number_bathrooms", "max_guest",
                    "price_by_night"]
        floats = ["latitude", "longitude"]
        """
        We create these two variables for when the user indicates any of
        these attributes within Place, and to be able to update their
        data to integers or floats according to where it corresponds
        """
        if len(args) == 0:
            print("** class name missing **")
        elif args[0] in class_personalize:
            if len(args) > 1:
                k = args[0] + "." + args[1]
                if k in models.storage.all():
                    if len(args) > 2:
                        if len(args) > 3:
                            if args[0] == "Place":
                                """
                                In this case, since Place has arguments
                                of integer and float type, than the other
                                classes no, then we corroborate that the
                                argument is within the corresponding
                                variables we create above and convert the
                                passed value in integer or float and then
                                save it
                                """
                                if args[2] in integers:
                                    if args[3]:
                                        args[3] = int(args[3])
                                    if not args[3]:
                                        args[3] = 0

                                elif args[2] in floats:
                                    if args[3]:
                                        args[3] = float(args[3])
                                    if not args[3]:
                                        args[3] = 0.0

                            setattr(models.storage.all()[k], args[2], args[3])
                            models.storage.all()[k].save()
                            """
                            We update the created class (eg Place)
                            adding only
                            ARGS 2 and 3. In this way, if the user spends more
                            args at the same time, only the
                            first
                            """
                        else:
                            print("** value missing **")
                    else:
                        print("** attribute name missing **")
                else:
                    print("** no instance found **")
            else:
                print("** instance id missing **")
        else:
            print("** class doesn't exist **")


if __name__ == '__main__':
    HBNBCommand().cmdloop()
