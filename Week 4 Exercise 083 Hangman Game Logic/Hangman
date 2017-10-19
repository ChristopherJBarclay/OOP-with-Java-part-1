public class HangmanLogic {

    private String word;
    private String guessedLetters;
    private int numberOfFaults;

    public HangmanLogic(String word) {
        this.word = word.toUpperCase();
        this.guessedLetters = "";
        this.numberOfFaults = 0;
    }

    public int numberOfFaults() {
        return this.numberOfFaults;
    }

    public String guessedLetters() {
        return this.guessedLetters;
    }

    public int losingFaultAmount() {
        return 12;
    }

    public void guessLetter(String letter) {  // 83.1
        // program here the functionality for making a guess
        // if the letter has already been guessed, nothing happens
        //i: if the letter has been guessed, it does not add letter to guessedLetters variable.

        // if the word does not contain the guessed letter, number of faults increases
        //i: increase number of faults only if... letter is not already guessed and letter is not in word
        //i: ((at end if none of the other if statements are true))
        // the letter is added among the already guessed letters.
        //i: always add letter to already guessed list, unless it was guessed before this method is called.

        if (guessedLetters.contains(letter)) {
            // if it is already guessed, do nothing.
        } else if (word.contains(letter)) {
            guessedLetters += letter;  //add guessed letter to guessedLetters variable if letter is not already guessed.
        } else {
            numberOfFaults++;
            guessedLetters += letter;
        }
    }

    public String hiddenWord() {
        // program here the functionality for building the hidden word
        // create the hidden word by iterating through this.word letter by letter
        // if the letter in question, from this.word, is within this.guessedLetters, put it in the hidden word
        // if the letter in question, from this.word, is not among guessedLetters, replace it with _ in the hidden word
        //i: run thru each letter in this.word and use guessedLetters.contains(letter) to see if current letter has been guessed.
        //i: if so, add it to hiddenWord. if not, add "_" to hiddenWord. then move onto the next letter


        // return the hidden word at the end
        int wordLength = word.length();
        String hiddenWord = "";

        for (int count = 0; count < this.word.length(); count++) {
            char thisLetter = this.word.charAt(count);
            String stringLetter = "" + thisLetter;

            if (guessedLetters.contains(stringLetter)) {
                hiddenWord += thisLetter;
            } else {
                hiddenWord += "_";
            }
        }
        return hiddenWord;
    }
}
