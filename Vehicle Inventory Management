#------------------------------------------------------------------------
# Program Name: Vehicle Inventory Program
# Author: Daniel J Nieman
# Date: Feb 8th, 2021
#------------------------------------------------------------------------
# Pseudocode: 1. Present user with application options
#             2. Option to add vehicle to inventory
#             3. Option to delete vehicle from inventory
#             4. Option to view inventory
#             5. Option to update inventory
#             6. Option to export inventory to Vehicle_Inventory.txt
#             7. Option to exti application
#------------------------------------------------------------------------
# Program Inputs:  1. Numeric input for menu options
#                  2. Vehicle input
#                     a. Make, model, color, year, mileage
#                  3. Vehicle deletion input by index position
#                  4. Invenotry update input by index postion and then
#                     Vehicle input
#           
# Program Outputs: 1. View of inventory list in application
#                  2. Inventory list as txt file "Vehicle_Inventory"
#------------------------------------------------------------------------

#Aautomobile class created.

class Automobile:

#Attributes listed.
    
    def __init__(self):
        self.__make = " "
        self.__model = " "
        self.__color = " "
        self.__year = 0
        self.__mileage = 0

#Object add_vehicle created and user inputs specified.

    def add_vehicle(self):
        self.__year = int(input("Enter year: "))
        self.__make = input("Enter make: ")
        self.__model = input("Enter model: ")
        self.__color = input("Enter color: ")
        self.__mileage = int(input("Enter mileage: "))

#String object created for user entry.
        
    def __str__(self):
        return ('%d %s %s Color: %s Mileage: %d' %
                (self.__year, self.__make, self.__model, self.__color,
                 self.__mileage))

#List created to store user inputs.
    
vehicle_list = []

#Edit object created to support Inventory Update function.

def edit(auto_list):
    print('\n')
    pos = int(input('Enter the position of the vehicle you want to edit: '))
    car.add_vehicle()
    new_vehicle = car.__str__()
    auto_list[pos - 0] = new_vehicle
    print('\n')
    print('Vehicle information has been updated.')

#User Menu is created and menu output options outlined.
user = True
while user:
    print("""
    1.Add a Vehicle
    2.Delete a Vehicle
    3.View Inventory
    4.Update Inventory
    5.Export Inventory
    6.Exit
    """)
    ans = input("Select from the options above: ")

#Supports instantiation of class Automobile, addining user input, in string form,
#to vehicle_list.
    
    if ans == "1":
        car = Automobile()
        car.add_vehicle()
        vehicle_list.append(car.__str__())

#First 'for' statement specifies enumeration of lsit items when invenotry is printed.
        
    elif ans == "2":
        for index, value in enumerate(vehicle_list, 0):
            print("{}. {}".format(index, value))

#list.pop() syntax used to delete vehicle's infor string based on index position.
            
        for i in vehicle_list:
            print('\n')
            vehicle_list.pop(int(input('Enter position of vehicle to remove: ')))
            print('\n')
            print('Successfully removed vehicle')
            break
#Print an enumerated list of vehicle inventory.
        
    elif ans == "3":
        for index, value in enumerate(vehicle_list, 0):
            print("{}. {}".format(index, value))

#Vehicle list printed before 'edit' object can be initiated.
            
    elif ans == "4":
        for index, value in enumerate(vehicle_list, 0):
            print("{}. {}".format(index, value))

        edit(vehicle_list)

#List items are written to a .txt Strings are separtated onto a new line.
        
    elif ans == '5':
        with open('Vehicle_Inventory.txt', 'w') as f:
            for items in vehicle_list:
                f.write("%s\n" % items)
        f.close()
        print("Inventory has been printed to Vehicle_Inventory.txt")

#Exit option, prints a salutation, terminates application.
    elif ans == '6':
        print("Thank you for using Automobile Inventory")
        break
    else:
        print('Please use one of the numbered options below: .')
