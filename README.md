
  

## Virgool Data


[![badge](https://img.shields.io/badge/npm-1.0.7-red.svg)](https://www.npmjs.com/package/virgool-data)  [![badge](https://img.shields.io/badge/license-MIT-yellow.svg)](https://github.com/imohamad/virgool-data/blob/master/LICENSE)  [![build passing](https://api.travis-ci.org/imohamad/virgool-data.svg?branch=master)](https://travis-ci.org/imohamad/virgool-data) [![Coverage Status](https://coveralls.io/repos/github/imohamad/virgool-data/badge.svg?branch=master)](https://coveralls.io/github/imohamad/virgool-data?branch=master)

  
  

package for getting data of posts and user profile from [virgool.io](https://virgool.io)

  

## Installation

  

`npm install virgool-data`

  

## Usage

  

    const virgoolData = require("virgool-data");
    
    //get posts data
    virgoolData.getPosts().then(posts => console.log(posts));
    
    //get user data - username must be without "@"
    //ex: const username = "imohamad";
    virgoolData.getProfile(username).then(user => console.log(user));


**posts output:**

    /* 
    get posts data
    virgoolData.getPosts().then(posts => console.log(posts));
    */
    
    //output:
         [
            {
                "title": string, //تیتر مطلب
                "link": string, //لینک مطلب
                "reading": string, //خواندن ۲ دقیقه
                "time": string, // ۲ هفته پیش
                "category": string, // دسته بندی مطلب
                "summary": string, // خلاصه مطلب
                "cover": string, // تصویر مطلب
                "like": string, // تعداد لایک
                "comments": string, // تعداد نظرات
                "author": {
                    "name": string, // نام نویسنده
                    "username": string, // نام کاربری نویسنده
                    "avatar": string // عکس پروفایل نویسنده
                }
            },
            {
              ...
            }
         ]
  

**profile output:**

    /* 
    get user data - username must be without "@"
    ex: const username = "imohamad";
    virgoolData.getProfile(username).then(user => console.log(user));
    */
    
    //output:
     [
            {
                "name": string, // نام نویسنده
                "username": string, // نام کاربری نویسنده
                "avatar": string, // عکس پروفایل نویسنده
                "bio": string, // بیوگرافی نویسنده
                "followers": string, // دنبال کنندگان نویسنده
                "following": string, // دنبال شونده های نویسنده
                "postCount": number, // تعداد مطالب منتشر شده نویسنده
                "posts": [
                    {
                        "title": string, // تیتر مطلب
                        "link": string, // لینک مطلب
                        "reading": string, // خواندن ۲ دقیقه
                        "time": string, // ۲ هفته پیش
                        "category": string, // دسته بندی مطلب
                        "summary": string, // خلاصه مطلب
                        "cover": string, // تصویر مطلب
                        "like": string, // تعداد لایک مطلب
                        "comments": string // تعداد کامنت های مطلب
                    }
                ]
            }
    ]
    




enjoy! 🤘

  

## Further help

  

visit [mohamad](https://mohamad.js.org) or send e-mail: [deylami.developer@gmail.com](mailto:deylami.developer@gmail.com)

