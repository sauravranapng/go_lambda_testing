To Deploy a sample  Go API to AWS Lambda and API Gateway



1.Create a lambda function 
    you need to import github.com/aws/aws-lambda-go/lambda and create a “handler”. 
    
    
2.Once the function has been created, you have to compile the code and create a ZIP for uploading it to AWS Lambda:

   commands- $Env GOOS="linux" go build main.go
   
   
3.create zip file of main.go

4.uplad zip to lambda created on aws

5.Add Trigger to lambda function

6.Click on the link to the API Gateway (not the API Endpoint) to open the settings of our Gateway

7.click on Models and “create”. Here, we can add a JSON Schema 

8.Now Click on Method Request, select Validate body on Request Validator and select the model we just created on Request Body.  turn Api key required -->true

9.Add API Keys-->we need to create usage plans
              -->Once API Key is created and assigned to an usage plan, we only need to pass it on our request as   a header with the name x-api-key.
 10.for detailed walkthrough refer-:   https://asanchez.dev/blog/deploy-api-go-aws-lambda-gateway/ 
