# Strength Prediction Tool

## Disclaimer
Please note that this is simply a proof of concept. Given the time constraints I faced this Summer with juggling a full-time job with full-time schooling, I did not spend the time including the following features I would have included, had it been the case that I had unbridled free time this Summer:
- Support for relevant demographics, such as Bodyweight, Age, Lifting Age, and Gender
- Individual models for numerous Bodyweight / Lifting Age / Gender categories
- Sufficient data to suppor the training of an unbiased model
- A more robust UI, including small features like delineation of current data points vs predicted data points
- A more advanced ML model (the lack of data created a situation such that spending time on fine tuning a dense neural net architecture didn't make sense)

## Setting the Project Up on Your Local Environment
To set the project up, we need to set up a local environment to provide a housing for all the dependencies of the project. To do this, we run `python3 -m venv tutorial-env`, and then, for Windows, we run `tutorial-env\Scripts\activate.bat` and for Unix/Mac `source tutorial-env/bin/activate`. From there, we can pip install all of the depencies for the project using `pip install <dependency-name>`.

## Running the Project
To run the project, we will move into our strength predictor directory by running `cd strengthpredictor` in the project's parent directory, and then we can run `python manage.py runserver`. This will run the web application. To retrain our model/update the data utilized in our model, we cd into the ml_model directory using `cd ../ml_model`, and we can use the python notebook called `ml_model.ipynb` to train a new model. Once the model is trained, we will move it into `strengthpredictor/authentication/my_model.pkl` and start the django server again.

## Errors and Limitations
Due to time constraints, I did not deploy this Django application to the web. While that could be easily achieved with sufficient time, I did not have the time, and it didn't make sense to deploy a proof of concept. Besides from the known deficiencies listed in the first section, I noticed a lot of the features were implemented in a rather hacky way, case A being my `view.py` file in `strengthpredictor/authencation`. I think that these could have been expressed in a more uniform/standardized way, given more time and knoweldge of Django. Overall, the main pitfalls of the project centered around not having sufficient data and not having sufficeint time to flesh out the project fully. I hope that the difficulty it requires to actually acquire all the powerlifting data for appropriate age and gender categories is taken into account. I think that the project shows a proof of concept for something potentially quite powerful and high in demand.