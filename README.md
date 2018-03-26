# read-kafka

Kafka sebagai messageing system. 

## Terminologi
    
    Broker - single node apps kafka

    Topic - Like a Table in RDBMS

    Consumer - yang nerima message dari Broker, Client yang berfungsi mengkonsumsi data dari topik tertentu. 1 thread consumer hanya dapat mengkonsumsi 1 partisi dari 1 topik. 1 Consumer dapat memiliki beberapa thread consumer

    Publisher - Client yang berfungsi mengirimkan data ke topik tertentu. 
    Jika topik memiliki lebih dari satu partisi secara default data akan diisikan 
    secara round robin namun producer dapat diatur untuk mengisi ke partisi tertentu dari suatu topic. 

    Replication Factor -  Seberapa banyak partiti itu di replkasi namun beda node. Fungsinya apa ?  

    Resilent Policy - Seberapa lama tersebut disimpan di kafka, jadi kafka itu sistemnya cuma ada append. 
    makanya dia cepet, bisa sampe 2jt messegse/s. Resilent Policy adalah kapan data itu akan dihapus, 
    bisa seberapa lama atau seberapa besar.

    Consumer Grup -  Group dari consumer. Fungsinya untuk apa ? Satu Consumer Group dapat terdiri dari satu consumer atau lebih.  Satu Consumer Group akan mengkonsumsi data dari satu topik tertentu. 
    Satu data tertentu hanya akan dikonsumsi satu kali oleh satu consumer group dan akan dikonsumsi oleh satu consumer tertentu didalam consumer group tersebut (consumer yang berbeda didalam satu consumer group tidak akan memperoleh data yang sama). 

    Partition, Bagaimana data itu di pecah. misal ada 1TB, mau dipartisi jadi 2. maka jadinya 500GB dan 500GB. Fungsinya apa ? Partisi berfungsi untuk mendukung proses paralel. Jumlah partisi yang lebih besar dapat meningkatkan throughput namun mengkonsumsi resource lebih banyak.


## Requirment

    1. Zookeeper
    2. Java 
    3. Kafka