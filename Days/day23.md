🛑 JSON Web Token aka #JWT ምንድን ነው?
JWT ለauthorization purpose (https://t.me/mrnazu/514) በሰፊው ጥቅም ላይ ይውላሉ so as a security expert እነሱን እንዴት መጠቀም እንደምንችል ማወቅ ጠቃሚ ነው ብዬ ስላሰብኩ ነው የተወሰነ ነገር share ላድርጋቹ ያሰብኩት።
.
🛑 JWT Structure:
JWT ሶስት ክፍሎች ሲኖሩት በdot(.) የተከፋፈሉ ናቸው።

1️⃣ Header: ያ token ምን አይነት #Algorithm አንደተጠቀመ የሚያሳይ ነው።
2️⃣ Payload: This Payload Part, describes certain properties of a user 
ማለትም ለምሳሌ:
 "name": "nazu",
 "admin": "false"
3️⃣ Signature or Key: the most important part ይሄ ነው ምክንያቱም እዚህ ጋር ከተሳሳትን server-ው የኛን JWT በጭራሽ አይቀበልም, ጥቅሙም token-ኑን verify ማደረግ ነው || for more check jwt.io

🛑 JWT Common Exploit

1️⃣ Manipulation 
encode የተደረገውን decode በማደረግ edit ማደረግ ነው። በጣም ቀላል መንገድ ነች🥸
ምሳሌ
{
"username":"nazu",
"isAdmin":"false"
}
ይሄን ወደ እዚ ልቀይረው😈
{
"username":"nau",
"isAdmin":"true"
}
2️⃣ Token #sidejacking or maybe #session #hijacking
የJWT token-ን or key-ን steal በማድረግ ራሳችንን validate ማስደረግ ነው🙂

3️⃣ Weak token key🚶
It's like a weak user password. It can easily be brute-forced by hackers.

Check this write up for better understanding

 (https://medium.com/@mrnazu/how-i-bypassed-the-jwt-task-from-the-xss-rat-ctf-e7dd241adc9d)👥Group @mrnazuu
📢 Channel @mrnazu

✍️Written by Nazu
