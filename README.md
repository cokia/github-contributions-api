# github-contributions-api

## TMI
 이 프로젝트를 활용해 특정 익스텐션을 개발하기위해 이 프로젝트를 포크했습니다.
 해당 익스텐션에 사용하기 위해 총 2곳에 배포 할 예정입니다.
 
### Disclaimer

This project is not intended for production use and should be shifted over into [sallar/github-contributions-api](https://github.com/sallar/github-contributions-api).

------

This api provides a json version of the contributions activity table on a github user's profile page. This was created because github does not provide an api for retrieving a users' total contributions.

Currently hosted on heroku: https://github-contributions-api.herokuapp.com

### Usage

`GET /:user/activity`

Returns whether or not user was active on a given day within the last year

```js
{
  "data": {
    "2016": {
      "9": {
        "25": false,
        "26": true,
        "27": true,
        "28": true,
        "29": true,
        "30": true
      },
      //...
    }
  }
}
```
----
`GET /:user/count`

Returns activity count of user on a given day within the last year

```js
{
  "data": {
    "2016": {
      "9": {
        "25": 0,
        "26": 10,
        "27": 6,
        "28": 3,
        "29": 7,
        "30": 6
      },
      //...
    }
  }
}
```

### Installation

Clone this repo:

```sh
git clone https://github.com/Didericis/github-contributions-api.git
```

Install node modules:

```sh
npm install
```

### Running

Development (will restart on code changes):

```sh
npm run start:dev
```

Production:

```sh
npm run start
```
