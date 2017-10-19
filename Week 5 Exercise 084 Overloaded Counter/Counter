public class Counter {
    public int startingValue;
    public int counter;
    public boolean check;

    public Counter() {
        this(0, false);
    }

    public Counter(boolean check) {
        this(0, check);
    }

    public Counter(int startingValue) {
        this(startingValue, false);
    }

    public Counter(int startingValue, boolean check) {
        this.startingValue = startingValue;
        this.check = check;
        this.counter = startingValue;
    }

    public int value() {
        return this.counter;
    }

    public void increase() {
        this.increase(1);
    }

    public void increase(int increaseAmount) {
        if (increaseAmount<0) {
            //do nothing if variable less than 0
        } else {
            this.counter+=increaseAmount;
        }
    }

    public void decrease() {
        this.decrease(1);
    }

    public void decrease(int decreaseAmount) {
        if (decreaseAmount<0) {
            //do nothing if variable less than 0
        } else {
            if (this.check) {
                this.counter-=decreaseAmount;
                if (this.counter<0) {        //if check is on, can't go below 0
                    this.counter = 0;
                }
            } else {
                this.counter-=decreaseAmount; //if check off, do no matter what
            }
        }
    }
}
