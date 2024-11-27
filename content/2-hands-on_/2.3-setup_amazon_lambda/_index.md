---
title: "Setup Amazon Lambda"
date: "`r Sys.Date()`"
weight: 7
chapter : false
pre: " <b> 2.3 </b> "
---

#### Create Telegram notification bot

1. Open Telegram Application. - |Could download <a href="https://telegram.org/">Here</a>|

2. Type **@BotFather** in the search box, and then setup:
	* Click Start button.
	* Type **/newbot**.
	* Type **<Name of bot\>**.
	* Type **<Username of bot\>** "username end with 'bot'".

	![](/images/Telegram_0.png?width=90pc)
3. Successful create a notification bot in Telegram application

#### Setup Amazon Lambda

1. Log in to the AWS Management Console admin page.

    ![](/images/Console_Home.png?width=90pc)

2. Type **Lambda** in the search box, and then select **Lambda**.

	![](/images/Open_Lambda.png?width=90pc)

3. Select **Layers** in **Additional resources** from the sidebar, then click on **Create layer** button.

	![](/images/Lambda_Create_Layer_1.png?width=90pc)

5.  For **Layer setup**:

	* Type the name of the layter in the **Name** field.
	* Choose **Upload a .zip file**.
{{% notice info %}}
You could choose **Upload a file file from Amazon S3** if file existed in S3
{{% /notice %}}
	* Click **Upload** button, then select file to upload.
	* Choose **x86_64** for **Compatible architectures**.
	* Choose **Python 3.9** for **Compatible runtimes**.
	* Then select **Create** button.

	![](/images/Lambda_Create_Layer_2.png?width=90pc)

{{%attachments title="Libraries files" style="orange" pattern=".*\.zip$"/%}}

6. Successful create a layer for Lambda funtion

	![](/images/Lambda_Create_Layer_3.png?width=90pc)

#### Create Lambda function

1. Select **Functions** from the sidebar, then click on **Create function** button.

    ![](/images/Lambda_Create_Function_0.png?width=90pc)

2. Type the name of the tuntion in the **Function name** field.

	![](/images/Lambda_Create_Function_1.png?width=90pc)

3. In Tab **Configuration**, select **Enviroment variables** from sidebar, then click **Edit** button to create enviroment variable.

	![](/images/Lambda_Add_Enviroment_0.png?width=90pc)

4. Click **Add enviroment variable** add new key, then type name of variable to **Key** field and value of variable to **Value** field. Click **Save** button to save edit.

	![](/images/Lambda_Add_Enviroment_1.png?width=90pc)

5. Select tab **Code**, then scroll down to bottom of page, and select **Add a layer** button in **Layers** section.

	![](/images/Lambda_Add_Layer_0.png?width=90pc)

6. In **Choose a layer** section:

	* Choose **Custom layers** in Layer source
	* Choose <name of created layer\>  in last step, and choose version.
	* Then click **Add** button.

	![](/images/Lambda_Add_Layer_1.png?width=90pc)

7. In **Function overview** of function, choose **Add trigger** button.

	![](/images/Lambda_Add_Trigger_0.png?width=90pc)

8. Choose **SNS** in combo box, and select **ARN of created topic**, then select **Add** button.

	![](/images/Lambda_Add_Trigger_1.png?width=90pc)

10. Successful add trigger to lambda function.

	![](/images/Lambda_Add_Trigger_2.png?width=90pc)

11. Select tab **Code**. In **Code source** section, paste code to lambda_function.py. Then select **Deploy** button to deploy code to Lambda.

	![](/images/Lambda_Add_Code_0.png?width=90pc)

{{%attachments title="Source files" style="orange" pattern=".*\.txt$"/%}}