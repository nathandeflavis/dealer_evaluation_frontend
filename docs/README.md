# dealer_evaluation_frontend
A product comparison application ('Final Project' in [Application Development using Microservices and Serverless](https://www.coursera.org/learn/applications-development-microservices-serverless-openshift) course, part of [IBM Full Stack Software Developer Professional Certificate](https://www.coursera.org/professional-certificates/ibm-full-stack-cloud-developer)).

<img width="922" alt="product_all_dealers_price" src="https://github.com/user-attachments/assets/51cee987-4d2c-462b-9135-9ba95d383aa9" />

Front-end in Apple macOS Safari.

# What does the project do?
## Scenario
Given repositories containing the code for backend microservices, my task was to deploy them using serverless (IBM Cloud Code Engine) and obtain URLs to access their respective API endpoints. Additionally, I cloned another repository containing the code for a front-end microservice. After deploying all microservices, I accessed the front-end application through its deployment URL. My task was to showcase the seamless integration of the microservices by providing screenshots of the final application.

## Review Criteria
1. Deploy the Microservice for Product Details.
2. Deploy the Microservice for Dealer Pricing.
3. Git-clone the Dealer Evaluation (Frontend) Microservice from the provided Git URL.
4. Change the code to point to the API endpoints in the placeholders, using the deployed URLs.
5. Deploy the Dealer Evaluation Frontend Microservice.
6. Open the deployment link.

# Why is the project useful?
The project is a chance to put my IBM Cloud Code Engine skills into practice.

# How can users can get started with the project?
You can run the application in [an IBM Skills Network lab environment](https://skills.network).

## Steps
### Deploy the Backend Microservices
1. Open the Code Engine CLI.
2. Deploy the microservice for Product Details: `ibmcloud ce application create --name prodlist --image us.icr.io/${SN_ICR_NAMESPACE}/prodlist --registry-secret icr-secret --port 5000 --build-context-dir products_list --build-source https://github.com/ibm-developer-skills-network/dealer_evaluation_backend.git`
3. Deploy the microservice for Dealer Pricing: `ibmcloud ce application create --name dealerdetails --image us.icr.io/${SN_ICR_NAMESPACE}/dealerdetails --registry-secret icr-secret --port 5000 --build-context-dir dealer_details --build-source https://github.com/ibm-developer-skills-network/dealer_evaluation_backend.git`

### Deploy the Frontend Microservice
1. In the terminal, go to `/home/project` directory: `cd /home/project`
2. Clone this repository in your `/home/project` directory: `git clone https://github.com/nathandeflavis/dealer_evaluation_frontend.git`
3. Change to the `dealer_evaluation_frontend` directory: `cd dealer_evaluation_frontend`
4. Deploy the Dealer Evaluation frontend microservice: `ibmcloud ce application create --name frontend --image us.icr.io/${SN_ICR_NAMESPACE}/frontend --registry-secret icr-secret --port 5001 --build-source .`
5. Open the link in the output.

# Where can users can get help with the project?
Users can contact the project's maintainers and contributors for help.

# Who maintains and contributes to the project?
@nathandeflavis

README adapted from [GitHub Docs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes).
