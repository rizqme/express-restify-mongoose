# express-restify-mongoose
This library provides mongoose database models with a REST interface. This is a fork of [express-restify-mongoose](https://github.com/florianholzapfel/express-restify-mongoose).
This fork adds support for custom methods.
## Getting started

Example

```javascript

restify.serve(router, Customer, {
    
    // new option: methods
    methods: {
        'customQuery': {
            method: 'GET',
            query: function(req, query) {
                return query.where(something).select(something);
            }
        },
        
        'customHandler': {
            method:'GET', // or PUT / POST / DELETE
            handler: function(req, res, next) {
                // add your custom middleware
            }
        }
    }
    
});

```

Then you can excute the following queries:

```
GET http://localhost/api/v1/Customers/customQuery
PUT http://localhost/api/v1/Customers/customHandler
```

## Contributors
* Enric León (https://github.com/nothingbuttumbleweed)
* David Higginbotham (https://github.com/dhigginbotham)
* Jonathan Greenemeier (https://github.com/6eDesign)
* Alan Levicki (https://github.com/alevicki)
* Michael (https://github.com/micheee)
* Matt Roman (https://github.com/romanmt)
* Fetrarijaona R. (https://github.com/fetrarij)
* Jan Paul Erkelens (https://github.com/jperkelens)
* Christoph Herbst (https://github.com/cherbst)
* doobinay (https://github.com/doobinay)
* Hareesh (https://github.com/hareeshbabu82ns)
* 09setht (https://github.com/09setht)
* Zertz (https://github.com/Zertz)
* Ph3n1x (https://github.com/Ph3n1x)
* Emre Efendioğlu (https://github.com/emreefendioglu)
* Tim Mckenzie (https://github.com/timmckenzie)
* Emil Janitzek (https://github.com/wiggin)
* Daniel Henrique Joppi (https://github.com/danieljoppi)
* Caleb Meredith (https://github.com/CalebMer)
* David Souther (https://github.com/DavidSouther)
* Marco Cameriero (https://github.com/95ulisse)
* Jan Melcher (https://github.com/Yogu)
* Urs Wolfer (https://github.com/uwolfer)
* Thomas Forrer (https://github.com/forrert)

## Formalia

```
Copyright (C) 2013 by Florian Holzapfel

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
