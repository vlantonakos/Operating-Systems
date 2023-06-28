```
procedure start_output(outdata: text; outcount: integer);
var
outindex: integer;
process print;
begin
while true do
begin
{await_printer_interrupt}
save_context;
ioport_dataout := outdata[outindex];
outindex := outindex + 1;
outcount := outcount - 1;
if outcount = 0
then
begin
disable_interrupts;
outdone := true
end;
restore_context
end {while}
end; {print}
begin {start_output}
outindex := 1;
outdone := false;
enable_interrupts
end; {start_output}
```
Ο παρεχόμενος κώδικας φαίνεται να είναι ένα απόσπασμα μιας διαδικασίας προγραμματισμού που είναι γραμμένη σε μια γλώσσα παρόμοια με ψευδοκώδικα. Ορίζει μια διαδικασία με το όνομα "start_output" που παίρνει δύο παραμέτρους: "outdata" τύπου κειμένου και "outcount" τύπου ακέραιος. Εδώ είναι μια ερμηνεία του τι κάνει ο κώδικας:
<ul>
    <li>Η διαδικασία αρχικοποιεί μια μεταβλητή με το όνομα "outindex" τύπου ακέραιος.</li>
    <li>Δηλώνει ένα διεργασία με το όνομα "print", η οποία δεν ορίζεται στο παρεχόμενο απόσπασμα του κώδικα.</li>
    <li>Η διαδικασία εισέρχεται σε έναν ατέρμονο βρόχο χρησιμοποιώντας την κατασκευή "while true do".</li>
    <li>Εντός της βρόχου, ο κώδικας αποθηκεύει το τρέχον περιβάλλον.</li>
    <li>Αντιστοιχεί την τιμή του "outdata[outindex]" σε μια μεταβλητή με το όνομα "ioport_dataout". Αυτό υποδηλώνει ότι η "ioport_dataout" είναι μια μεταβλητή που αντιπροσωπεύει ένα θύρα ή συσκευή εξόδου.</li>
    <li>Η τιμή του "outindex" αυξάνεται κατά 1.</li>
    <li>Η τιμή του "outcount" μειώνεται κατά 1.</li>
    <li>Εάν η τιμή του "outcount" γίνει μηδέν, ο κώδικας απενεργοποιεί τις διακοπές και θέτει μια μεταβλητή με το όνομα "outdone" σε true.</li>
    <li>Ο κώδικας επαναφέρει το προηγούμενα αποθηκευμένο περιβάλλον.</li>
    <li>Ο βρόχος συνεχίζει να εκτελείται απεριόριστα.</li>
</ul>

Η διαδικασία "start_output" ορίζει την αρχική τιμή του "outindex" ως 1 και του "outdone" ως false. Επίσης, ενεργοποιεί τις διακοπές.
