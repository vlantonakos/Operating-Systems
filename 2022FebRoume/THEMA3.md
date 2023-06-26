![image](https://github.com/vlantonakos/Operating-Systems/assets/107072477/8280fea7-1fdb-4c29-8cf6-fdacc670e518)

Για να απαντήσουμε σε αυτήν την ερώτηση, πρέπει να συγκρίνουμε το μέγεθος της λίστας ελεύθερων μπλοκ με το μέγεθος του χάρτη ψηφίων. Ας ορίσουμε τα εξής:

Δ = Αριθμός των bits για τις διευθύνσεις του δίσκου
Μ = Συνολικός αριθμός μπλοκ στον δίσκο
Ε = Αριθμός ελεύθερων μπλοκ στον δίσκο

Η λίστα ελεύθερων μπλοκ απαιτεί μνήμη για να αποθηκεύσει τις διευθύνσεις των ελεύθερων μπλοκ. Κάθε διεύθυνση απαιτεί Δ bits. Συνεπώς, η συνολική μνήμη που απαιτείται για να αποθηκευτεί η λίστα ελεύθερων μπλοκ είναι Ε * Δ bits.

Από την άλλη πλευρά, ο χάρτης ψηφίων απαιτεί ένα bit για κάθε μπλοκ στον δίσκο. Συνεπώς, ο συνολικός χώρος που απαιτείται για το χάρτη ψηφίων είναι Μ bits.

Για να ισχύει ότι η λίστα ελεύθερων μπλοκ χρησιμοποιεί λιγότερο χώρο από το χάρτη ψηφίων, πρέπει:

Ε * Δ < Μ

Αν το Δ έχει τιμή 16 bits, τότε η παραπάνω σχέση γίνεται:

Ε * 16 < Μ

Για να υπολογίσουμε το ποσοστό επί τοις εκατό, χρειάζεται να υπολογίσουμε την αναλογία μεταξύ του αριθμού των ελεύθερων μπλοκ (Ε) και του συνολικού αριθμού των μπλοκ (Μ):

Ποσοστό = (Ε / Μ) * 100

Συνεπώς, η απάντηση θα είναι το ποσοστό επί τοις εκατό που αντιστοιχεί στη συνθήκη:

Ε * 16 < Μ
Ποσοστό = (Ε / Μ) * 100

Παρακαλώ σημειώστε ότι πρέπει να γνωρίζουμε τις συγκεκριμένες τιμές των Μ και Ε για να υπολογίσουμε το ακριβές ποσοστό.