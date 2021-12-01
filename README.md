# Pokédex - Your guide to the world of Pokémon

![Image](./images/pokemon.png)

[![](./images/yt.png)](https://www.youtube.com/watch?v=ferXnJM0GI8)

## Table of Contents

* [Quick introduction](#quick-introduction)	
* [Scope](#scope)	
* [Setup](#setup)
* [Architecture](#architecture)
* [Technologies](#technologies)	
* [ERP SAP S/4 Hana](#ERP-SAP-S/4-Hana)	
* [SAPUI5](#SAPUI5)	
* [SAP Fiori](#sap-Fiori)	
* [CAP](#cap)	
* [I18n](#i18n)
* [Stack documentation](#Stack-documentation)


## Quick introduction

Pokédex is a website designed to catalogue and provide information about the various species of Pokémon, what's more it will be able to generate a team for you that will suit all your needs!
Scope

	- Website application should allow users to check Pokémon statistics such as  attack, defense, types, speed.
	- Main page should allow user to access all of its functionality.
	- Will have the ability to generate a Team of Pokémon- 6 Pokémon’s that are varied by types.
	- Create and delete your own Pokémon  with CRUD(Create, Read, Update, Delete) operation.
	- Statistics are updated by PokémonApi.
	- Application uses ERP system S/4 Hana as well as their technologies SAPUI5/OpenUI5 for User Interface  and Cloud Application Programming Model for server side (Back-end).
	- App will examine up to 120’000 request every hour. Database can contain up to 50’000  users and it can handle   up to 10’000 users logged in, in one moment. 
	- Pokédex will be hosted on a public cloud in the IaaS (Infrastructure as a Service) model using AWS (Amazon web service) or Microsoft Azure Cloud service 	infrastructure.
	- App allow to choose few language version e.g. English, Arabic, Japanese, Chinese, Norwegian, German, French, Polish, Russian, Czech 

### App won’t allow to:

	- Delete basic Pokémon’s
	- Adding or changing theme
	- Changing images of Pokémon’s
	- Manipulating Pokémon’s statistics
	- Modify database records 
	
## Setup
 To run this project, install it locally using npm:

```
 $ cd Projects
 $ npm install
 $ npm install sqlite3
 $ npm start
 $ cds watch 
```

## Technologies

 ### ![](./images/sap.png) ERP SAP S/4 Hana 

Belongs to the family of ERP systems, Hana is the newest SAP product. Released in 2015, it enables the use of the cloud and other operation of ERP systems such as planning and management human resources, processing large amounts of information etc. This solution is very future-oriented due to the date of withdrawal of support for older SAP systems in 2027. SAP provides its proprietary ultra-eficient database, which has proven itself in, among others, NBA, PKP, Harvard University etc.

### ![](./images/sapui5.png) SAPUI5

This frameworks helps design UI (User - interface). SAPUI5 based on design pattern MVC (Model-View-Controller) model. SAPUI5 uses JavaScript in ES6 version, XML (Extensible Markup Language) and HTML (HyperText Markup Language). Important layer of this framework is API Reference with ready to use components as carousel, tables, triggers, buttons etc. 
 

### ![](./images/fiori.png) SAP Fiori

Modern framework uses in design UX (User Experience) part of application. It’s based in similar technologies likes SAPUI5 


### ![](./images/js.png) JavaScript 
JavaScript is a dynamic computer programming language. It is lightweight and most used as a part of web pages, whose implementations allow client-side script to interact with the user and make dynamic pages. It is an interpreted programming language with object-oriented capabilities.

### ![](./images/xml.png) XML
An XML file is an extensible markup language file, and it is used to structure data for storage and transport. In an XML file, there are both tags and text.  XML is a markup language, which means it is a computer language that uses tags to describe components in a file.

### ![](./images/html5.png) HTML
HyperText Markup Language (HTML) is the set of markup symbols or codes inserted into a file intended for display on the Internet. The markup tells web browsers how to display a web page's words and images.


### ![](./images/cap.png) Cloud Application Programming model (CAP)

Server side of application (Backend) framework helps create, management server and services. Frameworks helps create CDS (Core Data Storage), services e.g. Authentication service, creating HTTP/HTTPS/FTP requests and  connect from UI to Server by Backend part of web application.

### ![](./images/nodejs.png) Nodejs 

JavaScript server-side version. Part of OpenJS Foundation. Nodejs packet manager is the same like JavaScript (npm). Handle single thread operation and execution code on V8 engine builded for Google Chrome. Similar as SAPUI5 uses MVC, MVCM etc. patterns. 


### ![](./images/sqlite3.png) SQLite3 

|Attribute	|Type				|Description
| --------------|-------------------------------|----------------------------------------------------------------|
|Name		|`String with 50 chars limit`	|Name of Pokémon
|ID		|`Integer`			|Pokémon number
|Type1		|`String with 50 chars limit`	|First type of Pokémon e.g. Electric
|Type2		|`String with 50 chars limit`	|Second type of Pokémon e.g. Grass
|Attack		|`Integer`			|	Pokémon attack
|Defense	|`Integer`			|	Pokémon defense
|Generation	|`Integer`			|	Pokémon generation
|HP		|`Integer`			|	Health point of Pokémon
|Legendary	|`Boolean`			|	If Pokémon is Legendary value is True else value is False
|Speed		|`Integer`			|	Pokémon speed attribute
|SpAttack	|`Integer`			|	Attack speed of Pokémon
|SpDefense	|`Integer`			|	Defense speed of Pokémon
|Total		|`Integer`			|	Total points
|modifiedAt	|`String with 100 chars limit`	|Describe when record was modified in format DD-MM-YYYY
|modifiedBy	|`String with 100 chars limit`	|Describe when record was modified in format DD-MM-YYYY
|createdAt	|`String with 100 chars limit`	|Describe when record was modified in format DD-MM-YYYY
|createdBy	|`String with 100 chars limit`	|Describe when record was modified in format DD-MM-YYYY


Every Pokemon is described by attributes from upper table To create a new Pokemon user need to describe pokemon by this attributes.   

### ![](./images/i18n.png) I18n 

To create multi-language application SAP system using i18n standard (Internationalization). Standard allow to matching language in browser language and changing application language to browser language. If app can’t find right language, app set default language e.g. default language for Pokedex is English.

 
Standard recognize correct language in name of file. Every language without default language have unique code which describe country e.g.  pl -> Poland, ru -> Russian, de-> German etc. 
Country codes can find at https://www.npmjs.com/package/i18n-iso-countries

## Stack documentation
|		Technology              |                     	Link                                |
|---------------------------------------|-----------------------------------------------------------|
| JavaScript	 			|`https://developer.mozilla.org/en-US/docs/Web/JavaScript`  |
| Node.js 				|`https://nodejs.org/en/docs/`                              |
| SAPUI5 				|	`https://sapui5.hana.ondemand.com/sdk/#/topic`      |
| Cloud Application programming model 	|`https://cap.cloud.sap/docs/`                              |
| SQLite3 				|`https://www.sqlite.org/docs.html`			    |
| PokémonAPI				|`https://documenter.getpostman.com/view/12403653/TVK8cLiK` |

