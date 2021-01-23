


Is het al Nawaka?
------------------





 Gepubliceerd: zaterdag 23 januari 2021 18:04
   





 NEE!
 








 // <![CDATA[
// Copyright (C) 2010 Ryan Wittering @ Webmaster Web - www.wmweb.nl
// URL: https://www.wmweb.nl/generators/javascript\_countdown
function do\_wmweb\_countdown\_wmweb\_countdown\_1501010148807()
{
// begin variabelen -
var na\_countdown = "De timer is afgelopen.";
var voorvoegsel = "Nog maar";
var achtervoegsel = "tot Nawaka 2022!";
var style = "";
var toon\_seconden = false;
var toon\_minuten = false;
var toon\_uren = false;
var toon\_dagen = true;
var stamp\_datum = 1659312000;
var divid = "wmweb\_countdown\_1501010148807";
// - einde variabelen
var stamp\_nu=Math.round(new Date().getTime()/1000);var sum=Math.round(stamp\_datum-stamp\_nu);
if(sum<=0){document.getElementById(divid).innerHTML="<span style=\""+style+"\">"+na\_countdown+"</span>";}
else{
var te\_tonen\_dagen=0;
if(toon\_dagen==true){
te\_tonen\_dagen=Math.ceil(sum/86400); //TODO als uren ook getoond gaan worden terug veranderen in floor
if(te\_tonen\_dagen>0){sum=Math.floor(sum%86400);}}

var te\_tonen\_uren=0;if(toon\_uren==true){te\_tonen\_uren=Math.floor(sum/3600);if(te\_tonen\_uren>0){sum=Math.floor(sum%3600);}}var te\_tonen\_minuten=0;if(toon\_minuten==true){te\_tonen\_minuten=Math.floor(sum/60);if(te\_tonen\_minuten>0){sum=Math.floor(sum%60);}}var te\_tonen\_seconden=0;if(toon\_seconden==true){te\_tonen\_seconden=sum;}var items=[];items[0]=[];items[0]['name']='dagen';items[0]['nameOne']='dag';items[0]['amount']=parseInt(te\_tonen\_dagen)-1;items[1]=[];items[1]['name']='uren';items[1]['nameOne']='uur';items[1]['amount']=parseInt(te\_tonen\_uren);items[2]=[];items[2]['name']='minuten';items[2]['nameOne']='minuut';items[2]['amount']=parseInt(te\_tonen\_minuten);items[3]=[];items[3]['name']='seconden';items[3]['nameOne']='seconde';items[3]['amount']=parseInt(te\_tonen\_seconden);var showedItems=[];for(i in items){var item=items[i];if(item['amount']!=undefined&&item['amount']>0){showedItems.push(item);}}var result="";for(i in showedItems){var showedItem=showedItems[i];i=parseInt(i);if(showedItem.amount!=undefined){if(i+1==showedItems.length&&i>0){result+=' en ';}else if(i>0){result+=', ';}result+=showedItem['amount']+' '+(showedItem['amount']==1?showedItem['nameOne']:showedItem['name']);}}}document.getElementById(divid).innerHTML="<span style=\""+style+"\">"+voorvoegsel+" "+result+" "+achtervoegsel+"</span>";
}
setInterval("do\_wmweb\_countdown\_wmweb\_countdown\_1501010148807();",1000);
// ]]>
 




 START: Modules Anywhere 
 Modules Anywhere Message: De module kan niet geplaatst worden omdat hij niet is gepubliceerd of toegewezen aan deze pagina. 
 END: Modules Anywhere 






