# Introduction To Amazon DynamoDB

Amazon DynamoDB is a type of database that works very fast — usually answering in just a few milliseconds — even when handling a lot of data. It’s fully managed by Amazon, which means you don’t have to worry about setting it up or maintaining it. It can store different kinds of data, like documents or simple key-value pairs.


In this lab activity, you will:

* Create an Amazon DynamoDB table.
* Enter data into an Amazon DynamoDB table.
* Query an Amazon DynamoDB table.
* Delete an Amazon DynamoDB table.


# STEP 1: CREATE A NEW TABLE

1.1 In the AWS Management Console, choose the  **Services** menu. Under **Database**, choose **DynamoDB** > Choose **Create table**.

1.2 For the **Table name**, enter _Music_

1.3 For the **Partition key**, enter _Artist_ and leave **String** selected in the dropdown list.

1.4 For **Sort key - optional**, enter Song and leave **String** selected.

1.5 Scroll down, and choose **Create table**.

The table will be created in less than 1 minute. Wait for the **Music** table to be **Active** before moving on to the next task.

# STEP 2: ADD DATA

2.1 Choose the **Music** table.

2.2 Choose **Actions**, and then choose **Create item**.

2.3 For the **Artist** value, enter _Pink Floyd_

2.4 For the **Song** value, enter Money

  These are the only required attributes, but you now add additional attributes.

2.5 To create an additional attribute, choose **Add new attribute**.

2.6 In the dropdown list, select **String**.

  A new attribute row will be added.

2.7 For the new attribute, enter the following:

  * **FIELD**: _Album_
  * **VALUE**: _The Dark Side of the Moon_

2.8 To add another new attribute, choose **Add new attribute**.

2.9 In the dropdown list, choose **Number**.

  A new number attribute will be added.

2.10 For the new attribute, enter the following:

   * **FIELD**: _Year_
   * **VALUE**: _1973_
     
2.11 Choose **Create item**.

   The item has now been added to the **Music** table.

2.12 Similarly, to create a second item, use the following attributes:






<img width="749" height="242" alt="image" src="https://github.com/user-attachments/assets/39432353-4830-4683-a1bd-7df4d58a3644" />




This item has an additional attribute called Genre. This is an example of each item being capable of having different attributes without having to pre-define a table schema.

2.13 To create a third item, use the following attributes:





<img width="748" height="241" alt="image" src="https://github.com/user-attachments/assets/4508f148-56ad-44da-886c-05a8f7d6b0b7" />





_Once again, this item has a new LengthSeconds attribute identifying the length of the song. This demonstrates the flexibility of a NoSQL database._

_There are also faster ways to load data into DynamoDB, such as using AWS Command Line Interface, programmatically loading data, or using one of the free tools available on the internet._


# STEP 3: MODIFY AN EXISTING ITEM

3.1 In the DynamoDB dashboard, under **Tables**, choose **Explore Items**.

3.2 Choose the **Music** button.

3.4 Choose **Psy**.

3.5 Change the Year from **2011** to **2012**.

3.6 Choose **Save changes**.

  The item is now updated.

# STEP 4: QUERY THE TABLE

There are two ways to query a DynamoDB table: _query_ and _scan_.

A query operation finds items based on the primary key and optionally the sort key. It is fully indexed, so it runs very fast.

4.1 Expand **Scan/Query items**, and choose **Query**.

  Fields for the Artist (Partition key) and Song (Sort key) are now displayed.

4.2 Enter the following details:

  * **Artist (Partition key)**: _Psy_
  * **Song (Sort key)**: _Gangnam Style_

4.5 Choose **Run**. 

4.6 Scroll up on the page, and choose **Scan**.

4.7 Expand **Filters**, and enter the following values:

  * For **Attribute name**, enter _Year_
  * For **Type**, choose **Number**.
  * For **Value**, enter _1971_

4.8 Choose **Run**

   Only the song released in 1971 is displayed.

# STEP 5: DELETE THE TABLE

5.1 In the DynamoDB dashboard, under **Tables**, choose **Update settings**.

5.2 Choose the **Music** table if it is not already selected.

5.3 Choose **Actions**, and then choose **Delete table**. 

5.4 On the confirmation panel, enter _delete_ and choose **Delete table**.

   The table will be deleted.


# WELL DONE!!

You now have successfully:

* Created an Amazon DynamoDB table
* Entered data into an Amazon DynamoDB table
* Queried an Amazon DynamoDB table
* Deleted an Amazon DynamoDB table

