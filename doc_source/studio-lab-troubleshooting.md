# Troubleshooting<a name="studio-lab-troubleshooting"></a>

The guide shows common errors that might occur when using Amazon SageMaker Studio Lab\. Each error contains a description, as well as a solution to the error\.

**Note**  
You cannot share your password with multiple users or use Studio Lab to mine cryptocurrency\. We don’t recommend using Studio Lab for production tasks because of runtime limits\.

 **Can’t access account** 

If you can’t access your account, verify that you are using the correct email and password\. If you have forgotten your password, use the following steps to reset your password\. If you still cannot access your account, you must request and register for a new account using the instructions in [Onboard to Amazon SageMaker Studio Lab](studio-lab-onboard.md)\. 

 **Forgot password** 

 If you forget your password, you must reset it using the following steps\. 

1.  Navigate to the [Studio Lab landing page](https://studiolab.sagemaker.aws)\.

1.  Select **Sign in**\.

1.  Select **Forgot password?**\. This opens a new page\. 

1.  Enter the email address that you used to sign up for an account\. 

1.  Select **Send reset link**\. This sends an email with a password reset link\. 

1.  From the password reset email, select **Reset your password**\. 

1.  Enter your new password\. 

1.  Select **Submit**\. 

 **Can't launch project runtime** 

If the Studio Lab project runtime does not launch, try launching it again\. If this doesn't work, switch the instance type from CPU to GPU \(or in reverse\)\. For more information, see [Change your compute type](studio-lab-manage-runtime.md#studio-lab-manage-runtime-change)\.

 **Runtime stopped running unexpectedly** 

If there is an issue with the environment used to run JupyterLab, then Studio Lab will automatically recreate the environment\. Studio Lab does not support manual activation of this process\. 

 **Conflicting versions** 

Because you can add packages and modify your environment as needed, you may run into conflicts between packages in your environment\. If there are conflicts between packages in your environment, you must remove the conflicting package\.

 **Environment build fails** 

When you build an environment from a YAML file, a package\-version conflict or file issue might cause a build to fail\. To resolve this, remove the environment by running the following command\. Do this before attempting to build it again\. 

```
conda remove --name <YOUR_ENVIRONMENT> --all
```

 **Increasing disk space in your project** 

If you get a notification that your disk space is full while you're attempting to create or import a file, you can delete files to increase space\. For instructions, see [Reset environment](studio-lab-use-manage.md#studio-lab-use-manage-conda-reset)\.