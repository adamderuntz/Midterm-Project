## Some Of My Code

from math import pi

def get_radius_from_user():
    while (True):
        try:
            radius = float(input("What is the radius: "))
            if (radius < 0):
                print("Radius must be a positive number.")
                continue
            break
        except ValueError:
            print("Only numbers may be entered.")

    return radius

def get_height_from_user():
    while (True):
        try:
            height = float(input("What is the height: "))
            if (height < 0):
                print("Height must be a positive number.")
                continue
            break
        except ValueError:
            print("Only numbers may be entered.")

    return height

def calculate_cylinder_volume(radius,height):
    volume = pi * radius ** 2 * height
    return volume

def generate_report(radius,height,volume):
    print("A right cylinder has a radius of", radius, "and the height is", height, "and has a volume of",volume)

def main():
        radius = get_radius_from_user()
        height = get_height_from_user()
        volume = calculate_cylinder_volume(radius, height)
        generate_report(radius,height,volume)

do_calculation = True
while (do_calculation):
    radius = get_radius_from_user()
    height = get_height_from_user()
    volume = calculate_cylinder_volume(radius, height)
    generate_report(radius,height,volume)
    another_calculation = input("Do you want to preform another calculation? (y/n) ")
    if (another_calculation != "y"):
        do_calculation = False


main()

