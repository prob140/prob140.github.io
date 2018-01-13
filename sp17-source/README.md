# Stat 140 Website

Access the live version at [prob140.org](http://probability.gitlab.io)

Based on Hyde (a Jekyll Theme)
![Hyde screenshot](https://f.cloud.github.com/assets/98681/1831228/42af6c6a-7384-11e3-98fb-e0b923ee0468.png)


## Contents

- Changing Data
- Building and Pushing
- Development


## Content Developers

The system is designed to make it as easy as possible to update the syllabus/ other content

### Updating Course Information

All information is stored inside the **_data** folder (everything else is a template, and not worth tampering with)


If you're trying to clone this website for another class (or if attempting to make modifications to course details - instructors, TAs, and tutor names), then modify **_data/courseInfo.yml**

If you're attempting to change the syllabus, everything is contained in the **_data/syllabus/** folder. The operations that you can do are

1) Adding a new week's worth of content by creating a new **yml** file in the **_data/syllabus/** folder (simply copy an existing *week.yml* file, and modify as required)

2) Adding lectures within a week, or updating links inside the course; simply change the required thing in the file 


## Building and Pushing 

1) Make sure you have Ruby installed (and gem as a result)
2) Install the required plugins
    
    gem install jekyll jekyll-paginate

3) run your own server
    
    jekyll serve

or 

4) Export to HTML

    jekyll build


## Development

The Prob 140 website is sourced from Hyde, and is built on top of Jekyll. We attempt to minimize the number of modules used, and most of the customization to the site comes from the data files. Have fun playing around


## License

Open sourced under the [MIT license](LICENSE.md).

<3
