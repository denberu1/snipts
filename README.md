# snipts
{
	"named function": {
		"prefix": "nfn",
		"body": [
		  "function ${1:functionname}($){",
		  "$3",
		  "}"
		],
		"description": "named function"
	  },
	  "arow function": {
		"prefix": "afn",
		"body": [
		  "const ${1:functionname}=($2)=>{",
		  "$3",
		  "}"
		],
		"description": "arow function"
	  },
	  "arrymethod": {
		"prefix": "op",
		"body": [
		  " ${1|forEach,map,reduce,filter|}((${2:item})=>",
		  "{",
		  "$3})",
		  ""
		],
		"description": "arrymethod"
	  },
	  "axios methods": {
		"prefix": "ax",
		"body": [
		  " axios.${1|post,get,put, delete|}('${2:url'})",
		  "      .then(res=>console.log(res.data))",
		  "        .catch(err=>console.log(err))",
		  ""
		],
		"description": "axios methods"
	  },
	  "express": {
		"prefix": "exp",
		"body": [
		  "const express =require('express');",
		  "  const app =express();",
		  " app.${1|post,get,put,delete|}('/${2:}',(req,res)=>{$});",
		  "const port=process.env.PORT||5000;",
		  " app.listen(port,()=>console.log(`SERVERN IS RUNNING AT ${port} );"
		],
		"description": "express"
	  },
	  "mongoose": {
		"prefix": "mongo",
		"body": [
		  "const mongoose = require('mongoose')",
		  "",
		  "const ${1:schemaname} = new mongoose.Schema({",
		  "    name: {type:String,required:true},",
		  "    photo: {type:String, required:true},",
		  "    price: {type:Number,required:true},",
		  "    countInStock:{type:Number,required:true,default:3},",
		  "    detail: {type:String,required:true},",
		  "    created_At: {type:Date,default:Date.now},",
		  "})",
		  "",
		  "const ${3:modelname} = mongoose.model('${4:modelename}', ${5:scemaname)",
		  "module.exports = ${6:modelename};"
		],
		"description": "mongoose"
	  }
}
 
