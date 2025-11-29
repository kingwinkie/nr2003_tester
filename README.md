# nr2003_tester


So as I am getting back into Papyrus NR2003. I seemed to have misplaced some CSV’s that I made for the tester~05.exe for nr2003.

So I do this to give me a idea of what I was doing in in the edit.  This is not fast but you can just start it and let it do it's thing

So how to see what the csv edits were doing to the exe.

While I use Darkers enabler, http://www.progress-tools.x10.mx/denabler.html you should be able to use anything that will let you show hidden buttons in a visual basic program

So for me I start denabler.exe and then I start tester_05.exe.

Drag and drop the red square onto the tester window. The denabler window should look something like this.

darker image

You should be able to see a list of items in the tester window that are there and wither they are visible or not.

If they have a little grey cube in front of them they are not showing.

I think they are all enabled by default. They are just not showing.

So right click on “ 00150718 “14” ThundeRT6TextBox “ in the  denabler window and click show you then should have a message saying “Successful “.

You only need to show two more buttons.

“ 00340890 “12” ThundeRT6TextBox “ in the  denabler window

and 

“ 00280788 “Search EXE” ThundeRT6CommandButton “ in the  denabler window.

The window should look like this

tester image

You should now be able to search for values in the exe. You may see a " not responding " message on tester but it is making a REALLY big txt file (see out.rar) so for a old vb program it will finish

If you input a range of -10000 in the first box and 10000 in the second it will find everything between those 2 values and output it to a csv file.

So click the Search EXE button and it will ask to open the exe (nr2003.exe) and then it will prompt for the file name to save to save a CSV file.

You can search for as big or small range as you want. The file size will vary on the size of the range. This will also work on the “old” 5MB nr2003.exe’s
 

After you have created your csv all you need to do is find what you are looking for :)

You should be able to use whatever you are comfortable with. Database /sql/excel/notepad++ etc and  even if the file is small enough windows notepad will search it.

I have included in this sample a bash file that should return the exe csv as well as the garage csv. The bash sh file should not only run on Linux it should also run under WSL and I have ran it under Git Bash on windows 10.

Right Click in the folder and select " Open Git Bash here "

When the promt opens type "bash run.sh "

This will run run.sh witch will inturn run garage.sh that will give you the values for " ~Original - Garage Settings - EXE.csv " and then it will run nr2003exe.sh that will return " ~Original - EXE.csv "

Gotcha's and things that happen

Tester will only try and return " sing " values so if the csv value is a doub or long the number will be " odd " . Now this is not much of a thing as it will always retung the same odd number. So the stock number for long/doub is also odd but it should always be the same.

"&H300D9" will return "Sing",9.10844E-44," when the ~Original - EXE.csv has a value of  65. So a stock value will always return Sing",9.10844E-44

&H value/lines missing and error's printing to console.

Error's are all/mostly about when it does not return a value there always seems to be at least one in  nr2003exe.sh also sometimes it just will drop a value and it just won't be there.

I did this fast and ugly but it seems to work "good enough" 

There are MORE things that can be enabled as well. So feel free to explore.

tester_more

Are there better ways oh yeah I’m sure but I am not a programmer (Just an old network admin/sysop and out of the biz for decades).

A real programmer should be looking at and doing this. :)


