<h1>Trasferimento dell'attenzione in reti GAN cicliche

Negli ultimi anni si è assistito a un notevole sviluppo nel settore tecnologico
per quanto riguarda l’intelligenza artificiale. Quest’ultima è ormai presente
nella maggior parte degli ambiti: dall’ambito medico, a quello industriale,
dalla creazione di bot capaci di aiutare l’uomo, all’elaborazione delle immagini. E proprio quest’ultimo ramo quello su cui si basa questo elaborato. ´
L’elaborazione e la generazione delle immagini sono una branca sulla quale il
Deep Learning sta lavorando assiduamente e sta producendo ottimi risultati.
Le tecniche utilizzate in questo campo sono molteplici e basano tutte il loro
funzionamento sulle reti neurali. Tra le reti utilizzate per questo scopo ci
soffermeremo sulle Cycle Consistent Generative Adversarial Networks (CycleGANs), una particolare evoluzione delle Generative Adversarial Networks
(GANs). Le CycleGANs pongono il proprio obiettivo nell’addestramento
simultaneo di due reti GAN all’interno di un ciclo, e vengono utilizzate nell’ambito della image-to-image translation. Lo scopo di una CycleGAN è,
quindi, quello di tradurre immagini appartenenti ad un dominio di input in
immagini appartenenti ad un dominio di output, e viceversa, cercando di generare immagini il più possibile realistiche e verosimili. L’idea fondamentale
su cui si basano le CycleGANs è detta consistenza del ciclo. Idealmente,
infatti, data un’immagine iniziale e applicandovi due volte il processo di traduzione, prima dal dominio iniziale a quello finale, e successivamente dal
dominio finale a quello iniziale, si ottiene un risultato uguale all’immagine di
partenza, generando così un ciclo che lega le traduzioni.
All’interno di questo elaborato vedremo nel dettaglio come funziona una CycleGAN, perché è così efficiente e, soprattutto, provvederemo ad un miglioramento dell’architettura su cui essa si basa, sfruttando l’algoritmo GradCam.
L’algoritmo GradCam non è altro che un algoritmo in grado di mostrare
graficamente il comportamento di una rete durante l’elaborazione di un’immagine. GradCam, infatti, è in grado di illustrare, grazie al gradiente della
rete, su quali punti dell’immagine la rete si focalizza maggiormente durante la generazione di un’immagine. Sfruttando questo concetto, che d’ora in
avanti chiameremo attenzione della rete, apporteremo delle modifiche alla
CycleGAN, introducendo, nel ciclo già citato, una consistenza non solo a livello di immagine, ma anche a livello di attenzione.
Per fare ciò , provvederemo inizialmente ad illustrare lo stato dell’arte, introducendo i concetti base di machine learning e addestramento di una rete, di
deep learning e reti neurali convolutive, fino ad illustrare le già citate GANs
e l’algoritmo GradCam. Successivamente, entreremo più nel dettaglio, andando a descrivere le CycleGANs da un punto di vista funzionale e a livello
di codice. Sempre in questo capitolo tratteremo, inoltre, il codice necessario
per implementare GradCam e, infine, proporremo una soluzione implementativa per l’utilizzo di GradCam durante l’addestramento di una CycleGAN.
Nel capitolo successivo, tratteremo i risultati ottenuti dalla rete così implementata, utilizzando i dataset horse2zebra e apple2orange. Concluderemo
l’elaborato, infine, illustrando i possibili sviluppi futuri applicabili al sistema
realizzato.
