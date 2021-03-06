# Lego Labels
<img src="http://i.imgur.com/a1jEr72.png" width="400">

Sort your LEGO like a pro

![Imgur](http://i.imgur.com/1exXDCp.png)

# Developing this

To get started quickly just:

* clone repo
* cd into it
* run `npm install` followed by `npm start`.

Alternativelly I recommend installing [enduro](http://www.endurojs.com/) globally by `npm i enduro -g`. This way you can just cd into the project and run `enduro`. This will also start development server at localhost:3000 with browsersync to live refresh scss, handlebars or javascript updates.

## Setting mongodb & rebrickable api

This project uses mongodb. I used [mlab](https://mlab.com/).

The mongodb connection url is not included in this repository to prevent abuse. You can sign up, it's free. Follow these steps to create your own mlab instance:

* sign up for [mlab account](https://mlab.com/signup/)
* click 'create new' to create new mongodb deployment
* mlab shows you the connection string, just add your credentials.

![](http://i.imgur.com/hXcEedm.png)

Also, don't forget to add your rebrickable api key to the same file.

Once you get the connection string you have to set it up either in enduro_secret.json or as a envirment variable. Create a file in root folder of this project called **enduro_secret.json** with this content:

```
{
	"secret": {
		"s3": {
			"S3_KEY": "",
			"S3_SECRET": ""
		},
		"DATABASE_URL": "<your mongodb connection url>",
		"REBRICKABLE_API_KEY": "<your rebrickalbe api key>"
	}
}
```
