## README

These are the files I used to create ePub and .mobi ebook formats from scratch. Note that these files were not created with any ebook-specific software, just a text editor. (Atom is a good one: https://atom.io)

You can download the finished product from this page: 
https://davidyeiser.com/fulltime-freelancer


### Note

- I've only done this on a Mac.
- Amazon's free tool Kindlegen is required to convert the ePub file to .mobi: 
https://www.amazon.com/gp/feature.html?docId=1000765211


### Instructions

In step one you are essentially creating a zip file with the file extension “epub”. Then you convert this to a .mobi file which can be read on a Kindle using Amazon's official converter tool.

#### Step 1

First, you create the ePub file with three Terminal commands. They need to be executed from within the uncompressed ePub directory.

````
zip -X filename.epub mimetype 
zip -rg filename.epub META-INF -x \*.DS_Store 
zip -rg filename.epub OEBPS -x \*.DS_Store
````

The end result will be filename.epub. And just to be clear “filename” is your file name. For example, mine was Full-time_Freelancer.epub.

#### Step 2

Then you can use Amazon’s KindleGen to convert the ePub to a .mobi file. Using terminal still, navigate to where the ePub file is. (If you haven't moved anywhere after creating it initially you don't have to do anything.) Run the following command:

````
kindlegen filename.epub
````

And _voilà,_ filename.mobi.