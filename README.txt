Codebase for NYGH Chatbot

The code is split into two different sections: Training and Deployment

requirements.txt: contains dependencies for the codebase, some might not be nesssary later on, depends on implmentation

Training:

- Training codes are included in the training folder
- data_augmentation.py: Used for data augmentation, incorparate nlpaug from Github to generate more data. TOUSE: Provide a NYGH.json that contains all the cetegories and patterns to be augmented and run python3 data_augmentation.py
- preprocessing.py: Helper used to clean raw data
- train_new: Use augmented_data.json generated from data_augmentation.py to train a chatbot model and save the model in the model folder


Deployment:
- deploy.py: Run deploy.py to host chatbot UI on localhost and testing. Folders templates and static are being used in deploy.py to support user interface. TO USE: python3 deploy.py
- predict.py: Helper used by deploy.py to utilize trained model and predict answer

NYGH.json and augmented_data.json will be required to run above code. A example of NYGH.json is provided in the directory.



REMOTE DEPLOYMENT:

Used heroku on testing remote deployment of the chatbot. The codebase here is too large for heroku to compile and deploy.

Created a separate github page here: https://github.com/geyi1/NYGH_chatbot_only for remote deployment, this repository is bascially the same, but without all the training code

To deploy with latest trained model, copy the newest chatbot_model_{}.h5, augmented_data.json, words.pkl, classes.pkl into the repository, and you can try on your own heroku account to deploy remotely.

