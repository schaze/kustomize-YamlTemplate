# kustomize-YamlTemplate
Template Plugin to extend input for configmaps and secrets. 
Requirements : bash, grep, sed, base64, shyaml, md5sum, awk
Offers:
 - Easy variable substitution           -- {{MY_VARNAME}}
 - Reading from user input              -- {{MY_VARNAME | READ}}
 - Reading from file                    -- {{MY_VARNAME | FILE:<filepath>}}
 - Reading from file with templating    -- {{MY_VARNAME | TEMPLATE_FILE:<filepath>}}
 - Base64 encoding for secrets          -- {{MY_VARNAME | BASE64}}
 
Options are combineable, e.g. to read a password from user input and encode it: {{MY_SECRET | READ | BASE64}}

Note:
  Plain text multiline file inputs are not supported yet (due to indentation)
  When using base64 encoding this is fine
