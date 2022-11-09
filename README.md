1.npm init -y
2.npm i eslint -D
3.npx eslint --init
4.npx eslint ./src

 1:13  error  Missing space before function parentheses      space-before-function-paren
 函数名与小括号间要有一个空格
  2:1   error  Expected indentation of 2 spaces but found 4   indent
  缩进是2个空格，但是却找到4个
  4:6   error  Newline required at end of file but not found  eol-last
  新行要求要另起一起


语法规范包类型
    不同组合：
        ESlint内置规范包：eslint-all(280多个规则）/eslint-recommended（60多个）
        标准规范包：eslint-config-standard（200多个）
        第三方规范包：google/airbnb/facebook


    第三方规范包：如airbnb
    https://www.npmjs.com/package/eslint-config-airbnb-base
    手动下载：
        查看需要下载的包和版本：npm info "eslint-config-airbnb-base@lastest" peerDependencies
    下载相关包：npx install -peerdeps --dev eslint-config-airbnb-base


配置规范包：
    1。修改eslint配置文件
    module.exports={
        "env":{
            "browser":true,
            "commonjs":true,
            "es2021":true
        },
        //"extends":"eslint:all",//内置，所有规则
        //"extends"""eslint"recommended",//内置，推荐规则
        "extends":"eslint-config-standard",//第三方，标准规则
        //"extends":"eslint-config-airbnb-base",//第三方，airbnb
        "parserOptions":{
            "ecmaVersion":12
        },
        "rules":{
            //
        }
    }