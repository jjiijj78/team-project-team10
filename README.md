# WhereShallWeMeet

Multi Location based gathering place recommendation service.

## TL;DR
http://165.194.35.214:13000

1. Input your want to do as keyword at `What you want to do?` box.
2. Click `AND` or `OR` button to combine your input keywords with conditions.
3. Click `새 위치 추가` button to add user starting place. (at least more than 2 places needed.)
Input alias name for place at first, then input 도로명 주소 or 지번 주소 for location in Korean.
4. Click `중간위치 찾기` button. done!


## History

##### Before commit : [f1525a3ba4daf517173fdaaf2c45b056117f8add](https://github.com/CAU-OSS-2019/team-project-team10/commit/f1525a3ba4daf517173fdaaf2c45b056117f8add)

*NaverAPIServer* <-> Client <-> Browser

- It ocurres CORS policy issues.
- It forces every single developers to contribute have to
  create their own NaverAPI.

*NaverAPIServer* <-> NodeJsExpress <-> Client <-> Browser

- It resolves CORS policy issues.
- Only NodeJsExpress needs to authenticate with *NaverAPIServer*

##### Before commit : [**30cb8ef1d00073be76937085d0c0a88fa8bfe685**](https://github.com/CAU-OSS-2019/team-project-team10/commit/30cb8ef1d00073be76937085d0c0a88fa8bfe685)

Using FelixSeol repository. Replace to CAU-OSS-2019/team-project-team10 


##### Before commit : [**54e960b9550083fcbad9718916d8070bce0300da**](https://github.com/CAU-OSS-2019/team-project-team10/commit/54e960b9550083fcbad9718916d8070bce0300da)

Change ~~Naver API~~ -> Kakao API



## Tutorial

### How to use Kakao Maps API with Proxy Server

- js/searchPlace.js

```JavaScript
function searchPlace(_keyword, _coordinate, _radius) {
    return new Promise(function (resolve, reject) {
        fetch(`http://165.194.35.214:26756/searchPlace/?keyword=${_keyword}&coordinate=${_coordinate}&radius=${_radius}`)
            .then(function (res) {
                // Response as Promise
                res.json().then(body => {
                    
                    /*To implement code with returned promise object.*/
                    
                }).catch(err => {
                    console.error(err);
                    reject("Error fetching.")
                });
            });
    })
}

```
