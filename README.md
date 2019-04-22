# LMSGI_04 - CHATBOT

## CHABOT 1

El primer chatbot té com a referencia l'exemple de Steve Worswick.

L'he traduit al català i personalment crec que dissenyar un chatbot per ser operat en angles, és molt mes senzill que fer-ho en català, o al manco la comunicació no sembla tan forçada.

He fet un [video](https://drive.google.com/file/d/1YkmBrA88zWoHOAwGUHJ05zLBVeYLDF6O/view?usp=sharing) amb converes amb el bot

Malgrat el video no té so, no es massa complicat veure i entendre el funcionament del bot:

1. Si iniciam la conversa amb un patró no reconegut pet bot, ens contesta que no pot processar la informació.
2. Si introduim un patro reconegut "Me pots informar sobre \*", on \* es allò sobre el que volem informació, per exemple: "Me pots informar sobre Madrid". En aquest cas:
   * El bot ens proporciona un link a la wikipedia de Madrid, en aquest cas.
   * S'ha declarat la variable lloc amb el valor Madrid.
3. Si repetim el mateix procés però amb els altres patrons ("Me mostres un mapa de \*" o "Quin temps fa en \*"), el bot ens proporcionara un link a un mapa o a la previsió del temps, i es el valor de la variable lloc canviara al segons la darrera petició realitzada.
4. Un cop declarada la variable lloc, el bot accepta altres tipus de converses:
   * "Parla sobre el lloc"
   * "Mostra el mapa del lloc"
   * "Tenen un bon dia alla"

En aquests casos i sempre que la variable lloc estigui declarada, el bot actuara com si haguessim introduit el patro inicial.
Es a dir, si la variable lloc=bilbao (pq.abans li hem demanat "Quin temps fa en Bilbao") i ara li demaman "Mostra el mapa del lloc", el bot actuara, com si la conversa introduida fos "Me mostres un mapa de Bilbao"

5. En canvi, si la variable lloc no està declarada i feim servir les converses dels punt 4 ("Parla sobre el lloc", "Mostra el mapa del lloc", "Tenen un bon dia alla"), el bot no pot actuar aplicant la primera conversa de cada model, sino que ens demana d'on volem informació, mapa o previsió climatica. Un cop li proporcionam el valor, la variable es declara i el bot pot respondre normalment.
