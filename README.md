Focus of This project:
    Via the users VIN # or YMM my app will give a user the ability to tell them their scheduled maintenance, how much the repair costs (with labor), the difficulty of the repair and if its OEM. Sends texts/emails when scheduled maintenance is approx by giving user prompts to find average mileage they do annually and then setting those approx timestamps they will be at next scheduled maintenace mileage point. Will direct you to nearest dealer for a part or a repair.

The Features (via VIN # or YMM of users vehicle):
    - Information of Vehicle Specs.
    - Information on DLC connector position in vehicle.
    - Information on upcoming repairs, their cost (labor included seperately), difficulty, and if OEM.
    - Informatin on nearest Dealer of users car make.
    - Sends texts/emails for approx timestamp of expected mileage so user is reminded (calculated by giving user prompts on regular commutes annually or 3rd party mileage integration if available?)
    - Users can register.
    - Users given car info is stored (vin # needs to be encrypted).
    - Users phone or email is stored for notification feature
    - Be helpful to people car hunting 

The Database Needs:
    Tables:
        -user: fields of id (pk), first_name, & last_name.
        - userContacts: fields of id(pk), user_id (fk), email (uk), phone_num (uk), address. Will contain the preferred method of contact as well (either phone or email)
        -userCredentials: id (pk), username (uk), password.
        -userCar: id (pk), user_car_id (fk), vin # (uk), mileage, car_year, car_make, car_model.
        -userMileagePrompt: this contains the answers for the prompt i will set for users to estime avg annual mileage.

The Prompts for Annual user mileage:
    -Do you work from home?
        This question will be an important one. One of the biggest use of mileage for people is work. If a user works from home then i will only need to calculate recreational miles. I also need to ask them if they are partial in office and from home(how many days a week if yes).
    -How many miles do you currently have on your vehicle?
    -How many miles did you put on your vehicle in the last 3 months?
    -How many miles did you put on your vehicle in the last 6 months?
    -How many miles did you put on your vehicle in the last year?
    -How many miles do you expect to drive your vehicle in the next year?
    -How many long road trips (over 200 miles each way) do you expect to take in the next year?
    -How many miles is your daily commute (round-trip)?
    -Do you often drive on hilly or mountainous terrain?
    -How often do you carry heavy loads or tow a trailer with your vehicle?
    -How often do you drive in stop-and-go traffic or in heavy congestion?

Types of CarMD API's:
    - Vehicle Spec info based off vin#
    - Vehicle Scheduled Maintenance
    - Ability to return data based on the code of the vehicle if connect to OBD port. If check engine light.
    - Vehicle Available and ongoing warranties
    - 

The formula for estimating gas mileage:
    This is to help calculate the users annual gas mileage.
    miles driven / gallons to refill the tank.