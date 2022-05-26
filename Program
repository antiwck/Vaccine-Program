import datetime

"""
                        New Patient Registration
-------------------------------------------------------------------------           --------------- 100 (MAX)
Vaccine     | Dosage required   | Interval Between Doses |    AgeGroup                      |   |
-------------------------------------------------------------------------                   |   |
    AF      |         2         |   2 weeks (or 14 days) | 12 and above             --------------- 45
    BV      |         2         |   3 weeks (or 21 days) | 18 and above                 |   |   |
    CZ      |         2         |   3 weeks (or 21 days) |   12 - 45                    |   |   |
    DM      |         2         |   4 weeks (or 28 days) | 12 and above             --------------- 18
    EC      |         1         |   -------------------- | 18 and above                 |   |
-------------------------------------------------------------------------           --------------- 12
                                                                                        CZ  AF  BV
                                                                                            DM  EC
"""

#_________________________________________________________________________________________________________________________________________________________________________________________________
# Prompt VCs input and assign uppercase to ensure lowercase input is acceptable and location will be false if input is "VC1" or "VC2" since it is an AND-logic and it will break out of loop
def get_location():
    message_for_location = "\nPlease select your location:-\n1) VC1\n2) VC2\nPlease select with number: "
    location = input(message_for_location)
    while location != "1" and location != "2":
        print("Error: Invalid selection")
        location = input(message_for_location)
    if location == "1":
        location = "VC1"
    else:
        location = "VC2"
    return location
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Eligible age is within 12 and 100, loop if input is out of range or recurve if not in numerical form, record if input is accurate
def get_age():
    message_for_age = "\nPlease enter your age within range of 12 to 100:-\nAge: "
    try:
        age = int(input(message_for_age))
        while (age < 12) or (age > 100):
            print("Error: Age must be between 12 and 100 else ineligible.")
            age = int(input(message_for_age))
        return age
    except ValueError:
        print("Error: Age must be in numerical form.")
        return get_age()
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Select vaccine based on age which will be return from age function
def vaccine_selection(age):
    if (age >= 12) and (age < 18):
        vaccine = input("\nPlease select your vaccine:\n1) AF\n2) CZ\n3) DM\nPlease select with number: ")
        while vaccine != "1" and vaccine != "2" and vaccine != '3':
            print("Error: Invalid vaccine.")
            vaccine = input("\nPlease select your vaccine:\n1) AF\n2) CZ\n3) DM\nPlease select with number: ")
        if vaccine == "1":
            vaccine = "AF"
        elif vaccine == "2":
            vaccine = "CZ"
        else:
            vaccine = "DM"
    elif (age >= 18) and (age <= 45):
        vaccine = input("\nPlease select your vaccine:\n1) AF\n2) BV\n3) CZ\n4) DM\n5) EC\nPlease select with number: ")
        while vaccine != "1" and vaccine != "2" and vaccine != '3' and vaccine != "4" and vaccine != "5":
            print("Error: Invalid vaccine.")
            vaccine = input("\nPlease select your vaccine:\n1) AF\n2) BV\n3) CZ\n4) DM\n5) EC\nPlease select with number: ")
        if vaccine == "1":
            vaccine = "AF"
        elif vaccine == "2":
            vaccine = "BV"
        elif vaccine == "3":
            vaccine = "CZ"
        elif vaccine == "4":
            vaccine = "DM"
        else:
            vaccine = "EC"
    else:
        vaccine = input("\nPlease select your vaccine:\n1) AF\n2) BV\n3) DM\n4) EC\nPlease select with number: ")
        while vaccine != "1" and vaccine != "2" and vaccine != '3' and vaccine != "4":
            print("Error: Invalid vaccine.")
            vaccine = input("\nPlease select your vaccine:\n1) AF\n2) BV\n3) DM\n4) EC\nPlease select with number: ")
        if vaccine == "1":
            vaccine = "AF"
        elif vaccine == "2":
            vaccine = "BV"
        elif vaccine == "3":
            vaccine = "DM"
        else:
            vaccine = "EC"
    return vaccine
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Name that contains other than alphabets will be required to input again
def get_name():
    name = input("\nPlease enter your name:-\nName: ").upper()
    while (any(character.isdigit() for character in name)):
        print("Error: Name contains number.")
        name = input("\nPlease enter your name:-\nName: ").upper()
    return name
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Retrieving gender using notation of "M" or "F" else rejected
def get_gender():
    gender = input("\nPlease enter your gender (M or F):-\nGender: ").upper()
    while gender != "M" and gender != "F":
        print("Error: Invalid gender.")
        gender = input("\nPlease enter your gender (M or F):-\nGender: ").upper()
    if gender == "M":
        gender = "MALE"
    else:
        gender = "FEMALE"
    return gender
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Minimum weight is assumed to be 40kg as minimum age for vaccination is 12. Weight that is invalid will be required to input again.
def get_weight():
    try:
        weight = float(input("\nPlease enter your weight (kg):-\nWeight: "))
        while weight <= 40:
            print("Error: Weight must be more than 40KG.")
            weight = float(input("\nPlease enter your weight (kg):-\nWeight: "))
        return str(weight)
    except ValueError:
        print("Error: Weight must be in numerical form.")
        return get_weight()
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# There are total of eight blood type, other than those, input will be rejected
def get_blood_type():
    blood_type = input("\nPlease enter your blood type:-\n1) A+\n2) A-\n3) B+\n4) B-\n5) AB+\n6) AB-\n7) O+\n8) O-\nPlease select above with number: ")
    while blood_type != "1" and blood_type != "2" and blood_type != "3" and blood_type != "4" and blood_type != "5" and blood_type != "6" and blood_type != "7" and blood_type != "8":
        print("Error: Invalid blood type.")
        blood_type = input("\nPlease enter your blood type:-\n1) A+\n2) A-\n3) B+\n4) B-\n5) AB+\n6) AB-\n7) O+\n8) O-\nPlease select above with number: ")
    if blood_type == "1":
        blood_type = "A+"
    elif blood_type == "2":
        blood_type = "A-"
    elif blood_type == "3":
        blood_type = "B+"
    elif blood_type == "4":
        blood_type = "B-"
    elif blood_type == "5":
        blood_type = "AB+"
    elif blood_type == "6":
        blood_type = "AB-"
    elif blood_type == "7":
        blood_type = "O+"
    else:
        blood_type = "O-"
    return blood_type
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Getting general medical history through number input, if not stated, user is allowed to entered personal medical history 
def get_medical_history():
    medical_input = input("\nMedical history:-\n1) Cardiovascular disease\n2) Respiratory disease\n3) Diabetes\n4) None\n5) Others (Please state)\nSelect above with number: ")
    while medical_input != "1" and medical_input != "2" and medical_input != "3" and medical_input != "4" and medical_input != "5":
        print("Error: Invalid medical input.")
        medical_input = input("\nMedical history:-\n1) Cardiovascular disease\n2) Respiratory disease\n3) Diabetes\n4) None\n5) Others (Please state)\nSelect above with number: ")
    if medical_input == "1":
        return "CARDIOVASCULAR DISEASE"
    elif medical_input == "2":
        return "RESPIRATORY DISEASE"
    elif medical_input == "3":
        return "DIABETES"
    elif medical_input == "4":
        return "NONE"
    else:
        medical_conditon = input("\nPlease enter your medical condition [r to return]: ").upper()
        if medical_conditon != "R" and any(character.isdigit() for character in medical_conditon) == False:
            return medical_conditon
        elif medical_conditon == "R":
            return get_medical_history()
        else:
            print("Error: Medical condition must not contain any number.")
            return get_medical_history()
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Contact can be either phone number or email where phone number has requirements else rejected but email is acceptable for any input
def get_contact():
    contact_method = input("\nPlease enter your contact method:-\n1) Phone number\n2) Email\nSelect above with number: ")
    while contact_method != "1" and contact_method != "2":
        print("Error: Invalid contact input.")
        contact_method = input("\nPlease enter your contact method:-\n1) Phone number\n2) Email\nSelect above with number: ")
    if contact_method == "1":
        contact = input("\nPlease enter your phone number [r to return]: ").lower()
        while contact != "r":
            if any(character.isalpha() for character in contact) or len(contact) < 10 or len(contact) > 11:
                print("Error: Invalid phone number (Phone number may contain alphabet, shorter than 10 digits or longer than 11 digits).")
                contact = input("\nPlease enter your phone number [r to return]:-\nPhone numer: ").lower()
            else:
                return str(contact)
        if contact == "r":
            return get_contact()
    else:
        contact = input("\nPlease enter your contact address [r to return]:-\nContact address: ").lower()
        if contact == "r":
            return get_contact()
        else:
            return str(contact)
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Assigned ID with prefix "WCK" and as individual register, ID will be given in sequence
def getID():
    with open("patients.txt", "r") as file:
        id_present = False
        for line in file:
            if line.startswith("Assigned ID        : "):
                latest_id = line[21:28]
                id_present = True
    if id_present == False:
        id = "WCK0000"
    else:
        temp_id = int(latest_id[3:7])
        temp_id += 1
        id = "WCK" + str(temp_id).zfill(4)
    return id
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Opening and writing all the details into the vaccination.txt and all details are converted to str before insertion
def get_details():
    print("""
________________________________________________

            NEW PATIENT REGISTRATION            
________________________________________________
""")

    location = get_location()
    age = get_age()
    vaccine = vaccine_selection(age)
    age = str(age)
    name = get_name()
    gender = get_gender()
    weight = get_weight()
    blood_type = get_blood_type()
    medical_history = get_medical_history()
    contact = get_contact()
    id = getID()
    
    print(f"""\n\nRegistration details:-\n\n1) Assigned ID     : {id}\n2) Location        : {location}\n3) Age             : {age}\n4) Vaccine         : {vaccine}\n5) Name            : {name}
6) Gender          : {gender}\n7) Weight(kg)      : {weight}kg\n8) Blood type      : {blood_type}\n9) Medical history : {medical_history}
10) Contact        : {contact}\n\nThank you for registering!\nYou may take your first vaccine dose at any time!""")
    
    patient_file_details = ["Assigned ID        : " + id,"Location           : " + location, "Age                : " + age, "Vaccine            : " + vaccine, "Name               : " + name,
    "Gender             : " + gender, "Weight(kg)         : " + weight + "kg", "Blood type         : " + blood_type, "Medical history    : " + medical_history, "Contact            : " + contact,]
    patient_file = open("patients.txt", "a")
    patient_file.write("\n")
    for element in patient_file_details:
        patient_file.writelines(element + "\n")
    patient_file.close()
    
    vaccination_file_details = ["Assigned ID        : " + id, "Location           : " + location, "Vaccine            : " + vaccine, "Name               : " + name, "Dose 1             : -",
    "Dose 2             : -", "Completion         : -"]
    vaccination_file = open("vaccination.txt", "a")
    vaccination_file.write("\n")
    for element in vaccination_file_details:
        vaccination_file.writelines(element + "\n")
    vaccination_file.close()
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Obtain all the info from given id
def get_info_from_id():
    
    with open("patients.txt", "r") as patient_file:
        exit_id = False
        found_in_patient_file = False
        while found_in_patient_file == False:
            check_id = input("\nPlease fill out following to continue procedure [r to return]\nID: ").upper()
            if check_id == "R":
                exit_id = True
                break
            else:
                id_line_in_patient_file = 0
                patient_file.seek(0)
                for line in patient_file:
                    id_line_in_patient_file += 1
                    if line.startswith("Assigned ID        : "):
                        patient_file_id = line[21:28]
                        if check_id == patient_file_id:
                            found_in_patient_file = True
                            location = (next(patient_file).strip()).removeprefix("Location           : ")
                            age = (next(patient_file).strip()).removeprefix("Age                : ")
                            vaccine = (next(patient_file).strip()).removeprefix("Vaccine            : ")
                            name = (next(patient_file).strip()).removeprefix("Name               : ")
                            gender = (next(patient_file).strip()).removeprefix("Gender             : ")
                            weight = (next(patient_file).strip()).removeprefix("Weight(kg)         : ")
                            blood_type = (next(patient_file).strip()).removeprefix("Blood type         : ")
                            medical_history = (next(patient_file).strip()).removeprefix("Medical history    : ")
                            contact = (next(patient_file).strip()).removeprefix("Contact            : ")
                            break
                if found_in_patient_file == False:
                    print("Error: Patient is not found.")
    
    if exit_id == True:
        return None, None, None, None, None, None, None, None, None, None, None, None, None, None, None
    else:
        with open("vaccination.txt", "r") as vaccination_file:
            found_in_vaccination_file = False
            while found_in_vaccination_file == False:
                id_line_in_vaccination_file = 0
                vaccination_file.seek(0)
                for line in vaccination_file:
                    id_line_in_vaccination_file += 1
                    if line.startswith("Assigned ID        : " + check_id):
                        found_in_vaccination_file = True
                        for items in range(3):
                            next(vaccination_file)
                        dose_1 = (next(vaccination_file).strip()).removeprefix("Dose 1             : ")
                        dose_2 = (next(vaccination_file).strip()).removeprefix("Dose 2             : ")
                        completion = (next(vaccination_file).strip()).removeprefix("Completion         : ")
                        break
        return check_id, location, age, vaccine, name, gender, weight, blood_type, medical_history, contact, dose_1, dose_2, completion, id_line_in_patient_file, id_line_in_vaccination_file
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Provide second appointment based on first appointment date and vaccine type
def get_second_appointment(vaccine):
    if vaccine == "AF":
        second_appointment = (datetime.datetime.today() + datetime.timedelta(days=14)).date()
        return str(second_appointment) + " which is 14 days from now"
    elif vaccine == "BV":
        second_appointment = (datetime.datetime.today() + datetime.timedelta(days=21)).date()
        return str(second_appointment) + " which is 21 days from now"
    elif vaccine == "CZ":
        second_appointment = (datetime.datetime.today() + datetime.timedelta(days=21)).date()
        return str(second_appointment) + " which is 21 days from now"
    else:
        second_appointment = (datetime.datetime.today() + datetime.timedelta(days=28)).date()
        return str(second_appointment) + " which is 28 days from now"
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Record vaccine administration and provide next appointment if dose 2 is required
def vaccination_administration():
    print("""
____________________________________________________

                VACCINE ADMINISTRATION              
____________________________________________________
""")
    id, location, age, vaccine, name, gender, weight, blood_type, medical_history, contact, dose_1, dose_2, completion, id_line_in_patient_file, id_line_in_vaccination_file = get_info_from_id()
        
    message_for_dose_administration_EC = "\nVaccine dose:-\n1) Dose 1\nDose 2 is not required for vaccine type 'EC'\nPlease select dose with number [r to return]: "
    message_for_dose_administration_AF_BV_CZ_DM = "\nVaccine dose:-\n1) Dose 1\n2) Dose 2\nPlease select dose with number [r to return]: "
    # This part is for vaccine EC
    if vaccine == "EC":
        dose_administration = input(message_for_dose_administration_EC).upper()
        while dose_administration != "1" and dose_administration != "R":
            print("Error: Invalid input.")
            dose_administration = input(message_for_dose_administration_EC).upper()
        
        if dose_administration == "R":
            pass
        else:
            if dose_1 == "COMPLETED":
                print("Your dose 1 has been completed previously.\nYou have completed all vaccination required for vaccine type 'EC'!")
            else:
                with open("vaccination.txt", "r") as file:
                    new_file_content = file.readlines()
                    new_file_content[id_line_in_vaccination_file + 3] = "Dose 1             : COMPLETED\n"
                    new_file_content[id_line_in_vaccination_file + 5] = "Completion         : COMPLETED\n"
                with open("vaccination.txt", "w") as file:
                    file.writelines(new_file_content)               
                print("Dose 1 has been administered.\nYour vaccination has been completed, Thank you very much.")
        
    # This part is for the rest of vaccine that requires second dose     
    elif vaccine == "AF" or vaccine == "BV" or vaccine == "CZ" or vaccine == "DM":
        dose_administration = input(message_for_dose_administration_AF_BV_CZ_DM).upper()
        while dose_administration != "1" and dose_administration != "2" and dose_administration != "R":
            print("Error: Invalid input.")
            dose_administration = input(message_for_dose_administration_AF_BV_CZ_DM).upper()
        
        if dose_administration == "R":
            pass
        elif dose_administration == "1":
            if dose_1 == "COMPLETED":
                print("Your dose 1 has been completed previously.")
            else:
                with open("vaccination.txt", "r") as file:
                    new_file_content = file.readlines()
                    new_file_content[id_line_in_vaccination_file + 3] = "Dose 1             : COMPLETED\n"
                with open("vaccination.txt", "w") as file:
                    file.writelines(new_file_content)               
                print("Dose 1 has been administered.\nYour first vaccination has been completed, Thank you very much.\nYour recommended date for second dose: " + get_second_appointment(vaccine) + "\n")

        else:
            if dose_1 != "COMPLETED":
                print("Your first dose has not yet been completed, please complete your first dose.\n")
            else:
                if dose_2 == "COMPLETED":
                    print(f"Your dose 2 has been completed previously.\nYou have completed all vaccination required for vaccine type '{vaccine}'!")
                else:
                    # Change the dose 2 and completion in vaccine file as completed
                    with open("vaccination.txt", "r") as file:
                        new_file_content = file.readlines()
                        new_file_content[id_line_in_vaccination_file + 4] = "Dose 2             : COMPLETED\n"
                        new_file_content[id_line_in_vaccination_file + 5] = "Completion         : COMPLETED\n"
                    with open("vaccination.txt", "w") as file:
                        file.writelines(new_file_content)     

                    print("Dose 2 has been administered.\nYour second vaccination has been completed\nYou have completed all of your vaccination!\nThank you!\n")
    else:
        pass
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Print out all the details of the patient from given id
def patient_record():
    print("""
____________________________________________________

        PATIENT RECORD AND VACCINATION STATUS       
____________________________________________________
""")
    id, location, age, vaccine, name, gender, weight, blood_type, medical_history, contact, dose_1, dose_2, completion, id_line_in_patient_file, id_line_in_vaccination_file = get_info_from_id()
    if id == None:
        pass
    else:
        if dose_1 == "-":
            dose_1 = "INCOMPLETE"
            dose_2 = "INCOMPLETE"
            completion = "NEW"
        elif dose_1 == "COMPLETED" and completion == "COMPLETED":
            pass
        else:
            dose_2 = "INCOMPLETE"
            completion = "COMPLETED-D1"
            
        print(f"""
Patient record and vaccination status:-\n
Assigned ID        : {id}
Location           : {location}
Age                : {age}
Vaccine            : {vaccine}
Name               : {name}
Gender             : {gender}
Weight(kg)         : {weight}
Blood type         : {blood_type}
Medical history    : {medical_history}
Contact            : {contact}
Dose 1             : {dose_1}
Dose 2             : {dose_2}
Status             : {completion}
""")
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Print information of VC1
def get_vc1_info():
    vc1_count, vc1_dose1, vc1_dose2, vc1_completed = 0, 0, 0, 0
    with open("vaccination.txt", "r") as file:
        for line in file:
            if line.startswith("Location           : VC1"):
                for items in range(2):
                    next(file)
                if next(file).startswith("Dose 1             : COMPLETED"):
                    vc1_dose2 += 1
                else:
                    vc1_dose1 += 1
                next(file)
                if next(file).startswith("Completion         : COMPLETED"):
                    vc1_completed += 1
                    vc1_dose2 -= 1
                vc1_count += 1
    print(f"""
___________________________________________________

                        VC1
___________________________________________________

Total amount of patient       : {vc1_count}
Waiting for dose 1            : {vc1_dose1}
Waiting for dose 2            : {vc1_dose2}
Completed                     : {vc1_completed}
___________________________________________________
""")
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Print information of VC2
def get_vc2_info():
    vc2_count, vc2_dose1, vc2_dose2, vc2_completed = 0, 0, 0, 0
    with open("vaccination.txt", "r") as file:
        for line in file:
            if line.startswith("Location           : VC2"):
                for items in range(2):
                    next(file)
                if next(file).startswith("Dose 1             : COMPLETED"):
                    vc2_dose2 += 1
                else:
                    vc2_dose1 += 1
                next(file)
                if next(file).startswith("Completion         : COMPLETED"):
                    vc2_completed += 1
                    vc2_dose2 -= 1
                vc2_count += 1

    print(f"""
___________________________________________________

                        VC2
___________________________________________________

Total amount of patient       : {vc2_count}
Waiting for dose 1            : {vc2_dose1}
Waiting for dose 2            : {vc2_dose2}
Completed                     : {vc2_completed}
___________________________________________________
""")
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Provide option to select information based on VC
def statistic():
    message_for_statistic = "\n\n" + "_" * 53 + "\n\n\t\tSTATISTICAL INFORMATION\n" + "_" * 53 + "\n\n" + "\nInformation of VC1 and VC2.\n1) VC1\n2) VC2\nPlease select VC to view statistical information: "
    option = input(message_for_statistic)
    while option != "1" and option != "2":
        print("\nError: Inavlid VC.")
        option = input(message_for_statistic)
    if option == "1":
        get_vc1_info()
    else:
        get_vc2_info()
#_________________________________________________________________________________________________________________________________________________________________________________________________


#_________________________________________________________________________________________________________________________________________________________________________________________________
# Main menu that prompts the program
def main_menu():
    message_for_main_menu = (f"""\n\n{"_" * 56}\n\n\tWELCOME TO MAIN MENU OF VACCINATION PAGE\n{"_" * 56}\n\n
    Please select the following:-\n1) New patient registration\n2) Vaccine administration\n3) Patient record and vaccination status\n4) Statistical information on vaccination\n
    [-1 to exit program]\nOption: """)
    option = input(message_for_main_menu)
    while option != "-1":
        if option == "1":
            get_details()
        elif option == "2":
            vaccination_administration()
        elif option == "3":
            patient_record()
        elif option == "4":
            statistic()
        else:
            print("Error: Invalid selection.")
        option = input("\nPress enter to continue to main menu [-1 to exit]\n").upper()
        while option != "" and option != "-1":
            print("Error: Invalid input.")
            option = input("\nPress enter to continue to main menu [-1 to exit]\n").upper()
        if option == "":
            option = input(message_for_main_menu)


    print("Program has terminated...")
#_________________________________________________________________________________________________________________________________________________________________________________________________

main_menu()
