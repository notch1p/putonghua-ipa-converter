# Putonghua IPA Converter

Convert Chinese texts to its Putonghua pronunciation in IPA form.

## Deploying

### Prerequisites(npm, A web server e.g. nginx)

### Compiling the backend

1. Clone the source code  
`git clone https://github.com/notch1p/putonghua-ipa-converter.git`  
`cd putonghua-ipa-converter`

2. Install dependencies  
`npm install rollup //append --global after install to use it globally`  
`npm install rollup-plguin-ts //specifically install it without --global`

3. Compile  
`npm run build`  
You can find your freshly built index.js in the root folder.

### Web Server Configuration  (nginx)  

only 2 files and **./data** are needed in this case:`index.js index.html`

```  
    location /
    {
        alias <absolute-path-to-your-webroot-folder>; #which should contain index.html
        index index.html;
    }
    location  ~ .*\.(jpg|jpeg|gif|png|ico|css|js|pdf|txt)$
    {
      root <absolute-path-to-thefolder-containing-index.js>
    }
```  

You should be good to go now.
