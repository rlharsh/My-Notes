<%*
noteContent = await tp.file.selection();
let numberOfStrings = noteContent.split('\n').length;
let titre;
let corps;
if (numberOfStrings === 1) {
titre = noteContent.match(/.*/g)[0];
} 
*%>