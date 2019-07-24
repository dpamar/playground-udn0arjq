# Javascript template

Again, even if you're not familiar with JS, it should be understandable :)

Note : this is a Lambda function implemented using JS, to be executed in any browser Developer tools console

```javascript
/** HEADERS **/
(MultiQuine=language=>{
 data={};
 /** DATA **/
 data['BF']=[/** BF code goes here **/];
 data['CS']=[/** CS code goes here **/];
 data['JS']=[/** JS code goes here **/];
 /** CODE **/
 if(!language)language='JS';
 res='';
 i2c=x=>String.fromCharCode(x);
 nl=i2c(10);
 switch(language)
 {
  case 'BF':
   res += [/** BF headers block goes here **/].map(i2c).join('');
   res += ['BF','CS','JS'].map(x=>x.split('').map(y=>'+'.repeat(y.charCodeAt())+'>').join('')+'>'+data[x].map(y=>'+'.repeat(y)+'>').join('')+'>').join('');
   break;
  case 'CS':
   res += [/** CS headers block goes here **/].map(i2c).join('');
   res += ['BF','CS','JS'].map(x=>'        data.Add("'+x+'", new int[]{'+data[x].join(',')+'});'+nl).join('');
   break;
  case 'JS':
   res += [/** JS headers block goes here **/].map(i2c).join('');
   res += ['BF','CS','JS'].map(x=>" data['"+x+"']=["+data[x].join(',')+"];"+nl).join('');
   break;
 }
 res+=data[language].map(i2c).join('');
 return res;
})
```
