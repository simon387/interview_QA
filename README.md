# interview_QA

## JAVA

**Q: Cosa è un POJO?**

A: Descrive una classe che non ha bisogno di essere una sottoclasse di qualcosa o implementare interfacce specifiche. Ha proprietà private e metodi di accesso
pubblici.

---

**Q: JPS?**

A: Java Virtual Machine Process Status Tool, è stato introdotto con java 1.5. Elenca le JVM attive sul SO. Se JPS viene eseguito senza specificare un hostid,
cercherà JVP attive sull'host locale. Inoltre ha quasi sostituivo l'uso ```ps -ef|grep java```.

---

**Q: CDA?**

A: Class Dependency Analyzer; **jdeps** è uno strumento da riga di comando introdotto in JDK 8 per comprendere le dipendenze statiche e le librerie
dell'applicazione, ad esempio il comando **jdeps** mostra le dipendenze a livello di pacchetto o di classe dei file di classe Java. L'input per jdeps può essere
un nome percorso file .class, un file JAR o può essere un nome di classe completo per analizzare tutti i file di classe. Ogni volta che forniamo input allo
strumento, questo genera le dipendeze alla console.

---

**Q: Mockito?**

A: framework che permette di creare oggetti mock a partire sia da una interfaccia che da una classe semplicemente dichiarandone il comportamento.

---

**Q: Selenium**

A: tool open-source per l'automazione di browser, permette di specificare istruzioni per automatizzare le interazioni con il sito; il componente **Selenium
WebDriver**, permette di registrare modificare e debuggare test per web application.

---

**Q: Funzioni LAMBDA**

A: Funzionalità da Java SE 8. E' un metodo senza una dichiarazione, scorciatoia che consente di scrivere un metodo nello stesso posto dove serve. Le lambda
expression sono particolarmente utili nei casi in cui serve definire una breve funzione che ha poche linee di codice e che verrà utilizzata una sola volta.

Le classi anonime interne forniscono un modo per implementare classi che vengono utilizzate una sola volta.

Le interfacce funzionali (Java 8), come ActionListener, EventListener, Runnable, Comparator, FileFilter sono caratterizzate dalla presenza di un solo metodo e
si prestano bene per l'utilizzo delle Lambda Expression.

Es. ordinamento lista interi usando **Comparator** (interfaccia funzionale - compare())

Normale:

```
Collections.sort(numbers,new Comparator<Integer>(){
    @Override
    public int compare(Integer o1,Integer o2){
        return o1.compareTo(o2);
    }
}
```

Lambra Expression:

```
Collections.sort(numbers, (Integer o1, Integer o2) -> {return o1.compareTo(o2)});
```

---

**Q: Parallel Stream**

A: il metodo **parallelStream()** (java 8) esegue le operazioni sugli elementi in parallelo. Gli **Stream** non sono riusabili perchè sono pensati per poter
eseguire una serie finita di operazioni sui loro edi una lementi; è possibile quindi istanziare uno Stream e usare la sua referenza con tutte le intermediate
operation, ma l'esecuzione termina l'operation lo rende inacessibile. Inoltre un paralle stream può essere riconvertito in sequenziale in ogni momento con il
metodo **sequential()**.

Regola: le intermediate operation (**filter()**, **distinct()**) vanno messe sempre prima delle operazioni e sono __lazy__, vengono eseguite solo se sono
necessarie per l'esecuzione della terminal operation.

es: terminal operation ```listacolori.stream().sorted().anyMatch()```

Il seguente codice crea un parallel stream di numeri interi:

```
List<Integer> numeri = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);
int somma = numeri.parallelStream()
    .filter(n -> n%2 == 0)
    .mapToInt(Integer::intValue)
    .sum();
```

In questo esempio, la lista di numeri viene trasformata in un paralle stream; successivamente viene applicata una serie di operazioni di filtraggio e di
mappatura, infine la somma.

La principale differenza con uno stream normale è che un parallel stream può eseguire le operazioni in parallelo usando più thread. Tuttavia, l'utilizzo può
comportare dei costi aggiuntivi, come la sincronizzazione dei thread, il che significa che non sempre è la scelta migliore.

---

## General

**Q: JSON?**

A: JS Object Notation, formato testuale per la strutturazione e scambio dati tra applicazioni client server, valida alternativa a XML

---

**Q: Thread?**

A: è un processo che appartiene ad un programma o ad un altro processo. Due o più thread possono condividere, indipendentemente dai dati, il codice che essi eseguono. Questo avviene quando tali thread eseguono il loro codice da istanze della stessa classe.

---

**Q: Session?**

A: si intende un gruppo di interazioni con un sito web in un determinato arco di tempo. Ad esempio una singola sessione può contenere più visualizzazioni di pagina, eventi, interazioni, ecc...

Un singolo utente può aprire più sessioni, nell'arco di diverso tempo; una sessione termina dopo un tempo di inattività predefinito.

---

**Q: DNS?**

A: Domain Name System, traduce indirizzi web, nomi, in indirizzi IP.

---

**Q: HTTP / HTTPS / Header?**

A: Hiper Text Transfer Protocol, protocollo di comunicazione utilizzato per il trasferimento della pagine web. Un server HTTP generalmente resta in ascolto delle richieste dei client sulla porta 80 usando il protocollo TCP a livello di trasporto. Le specifiche sono gestite dal World Wide Web Consortium (WC£).

La principale differenza tra HTTP e HTTPS è che quest'ultimo utilizza un protocollo di sicurezza SSL/TLS (Secure Sockets Layer/Trasnsport Layer Security) per cifrare i dati trasmessi.

---

---

---

---

---

---

---

---

---

---














