# Convert dd-mm-yyyy to mm-dd-yyyy in Excel
#### If your Excel file reads mm/dd/yyyy dates as dd/mm/yyyy, you can fix it by:

1️⃣ Selecting the cells

2️⃣ Right-click → Format Cells → Date → Pick your desired format

Or, use a formula like =TEXT(A1,"mm/dd/yyyy") to convert it manually.

Another option is =DATEVALUE(A1) 

But if you’ve tried all of that and it still shows as text or throws a #VALUE! error when using =DATEVALUE(A1), it’s likely because the text value isn’t aligned with your system’s date and time settings.

Here’s a quick trick you can try:

Since it’s just a string, you can rearrange the parts of the date string into the correct order using a formula.

Example:

![Screen Shot 2025-05-04 at 2 50 20 PM](https://github.com/user-attachments/assets/a7ae0473-bea6-4a5b-8df2-0058ba96eabd)

I rearrange the string using this formula: =MID(A2,4,2)&"/"&LEFT(A2,2)&"/"&RIGHT(A2,4) to the right order.

Then, copy and paste only the value.

![Screen Shot 2025-05-04 at 2 52 19 PM](https://github.com/user-attachments/assets/5a79fc4b-7d11-46e3-ae2d-274daa9ff09c)

The data will be date format as shown:

![Screen Shot 2025-05-04 at 2 54 56 PM](https://github.com/user-attachments/assets/8e9513dc-92b0-4955-bef4-8e0ba7189dda)

Super handy when dealing with stubborn date data!

Hope this little tip will help you.
