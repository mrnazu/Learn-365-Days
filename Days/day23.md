π JSON Web Token aka #JWT ααα΅α αα?
JWT αauthorization purpose (https://t.me/mrnazu/514) α α°αα α₯αα αα­ α­ααα so as a security expert α₯αα±α α₯αα΄α΅ αα αα α₯αα°ααα½α ααα α αα αα α₯α¬ α΅αα°α₯α© αα α¨α°αα°α ααα­ share αα΅α­ααΉ α«α°α₯α©α΅α’
.
π JWT Structure:
JWT αΆα΅α΅ α­ααα½ α²αα©α΅ α dot(.) α¨α°α¨ααα ααΈαα’

1οΈβ£ Header: α« token αα α α­αα΅ #Algorithm α αα°α°α αα α¨αα«α³α­ ααα’
2οΈβ£ Payload: This Payload Part, describes certain properties of a user 
ααα΅α ααα³α:
 "name": "nazu",
 "admin": "false"
3οΈβ£ Signature or Key: the most important part α­α αα αα­αα«α±α α₯αα αα­ α¨α°α³α³α΅α server-α α¨αα JWT α α­α«α½ α α­αα αα, α₯ααα token-αα verify αα°α¨α αα || for more check jwt.io

π JWT Common Exploit

1οΈβ£ Manipulation 
encode α¨α°α°α¨ααα decode α αα°α¨α edit αα°α¨α ααα’ α α£α ααα αααα΅ αα½π₯Έ
αα³α
{
"username":"nazu",
"isAdmin":"false"
}
α­αα αα° α₯α ααα­α¨απ
{
"username":"nau",
"isAdmin":"true"
}
2οΈβ£ Token #sidejacking or maybe #session #hijacking
α¨JWT token-α or key-α steal α αα΅α¨α α«α³α½αα validate αα΅α°α¨α ααπ

3οΈβ£ Weak token keyπΆ
It's like a weak user password. It can easily be brute-forced by hackers.

Check this write up for better understanding

 (https://medium.com/@mrnazu/how-i-bypassed-the-jwt-task-from-the-xss-rat-ctf-e7dd241adc9d)π₯Group @mrnazuu
π’ Channel @mrnazu

βοΈWritten by Nazu
