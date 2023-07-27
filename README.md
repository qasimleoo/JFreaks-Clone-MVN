## baking ##
use following command to bake  
`mvn jbake:generate`  
## minification ##
there are separate plugins for jbake-maven build and for minification
and different commands will be used to bake and minify. minification is not the part of jbake lifecycle.
So, always run commands of baking first then minify the static assets.If we run minify command and then bake, static 
assets will not be minified.Following command will be used to minify css:  
`mvn yuicompressor:compress`  
In order to minify js files, use following command  
`mvn closure-compiler:minify`  
## Live Server ##
following command will bake and run on server at port 8820. static files will not be minified.  
`mvn jbake:inline`  
Further you can read on [Github](https://github.com/jbake-org/jbake-maven-plugin)  

## build Folder ##
all outputs of build are in `target` folder which is in project root path and maven default build directory.
so,if maven lifecycle commands will also work but could make conflicts in generating output. So, try to run only
commands which are mentioned here. we can delete target folder by `mvn clean` command.  


