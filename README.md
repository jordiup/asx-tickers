# asx-tickers

This repo contains a JSON array of 2930+ ASX Companies

The format is as follows (Ticker - Company Name):

```
[
	"14D - 1414 DEGREES LIMITED",
	"1AD - ADALTA LIMITED",
	"1AG - ALTERRA LIMITED",
	"1ST - 1ST GROUP LIMITED",
	"1VG - VICTORY GOLDFIELDS LIMITED",
	"29M - 29METALS LIMITED",
...   
```

Downloaded from 
- https://www2.asx.com.au/markets/trade-our-cash-market/directory
- (or) https://asx.api.markitdigital.com/asx-research/1.0/companies/directory/file?access_token=83ff96335c2d45a094df02a206a39ff4

These can be fetched from the client side using the below native html/js

```
     var requestOptions = {
        method: 'GET',
        headers: {
            accept: '*/*',
            'accept-language': 'en-AU,en-US;q=0.9,en;q=0.8',
            'sec-fetch-dest': 'empty',
            'sec-fetch-mode': 'cors',
            'sec-fetch-site': 'cross-site',
        },
        referrerPolicy: 'strict-origin-when-cross-origin',
        method: 'GET',
        mode: 'cors',
        credentials: 'omit',
        redirect: 'follow',
    };
    
    fetch(
        'https://raw.githubusercontent.com/jordiup/asx-tickers/main/tickers-with-name.min.json',
        requestOptions,
    )
        .then((response) => response.json())
        .then((result) => {
          // Do what you want here...
        })
        .catch((error) => console.log('error', error));
```
