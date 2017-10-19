import java.util.Calendar;

public class Person {
    private String name;
    private MyDate birthday;
    
    public Person(String name, int day, int month, int year) {
        this.name = name;
        this.birthday = new MyDate(day, month, year);
    }

    public Person(String name, MyDate birthday) {
        this.name = name;
        this.birthday = birthday;
    }

    public Person(String name) {
        this.name = name;
        int todaysDay = Calendar.getInstance().get(Calendar.DATE);
        int todaysMonth = Calendar.getInstance().get(Calendar.MONTH) + 1; // January is 0 so we add one
        int todaysYear = Calendar.getInstance().get(Calendar.YEAR);
        this.birthday = new MyDate(todaysDay,todaysMonth,todaysYear);
    }
    
    public int age() {
        // calculate the age based on the birthday and the current day
        // you get the current day as follows:
        int todaysDay = Calendar.getInstance().get(Calendar.DATE);
        int todaysMonth = Calendar.getInstance().get(Calendar.MONTH) + 1; // January is 0 so we add one
        int todaysYear = Calendar.getInstance().get(Calendar.YEAR);
        MyDate todaysDate = new MyDate(todaysDay, todaysMonth, todaysYear);

        int compareNumOfDays = this.birthday.differenceInYears(todaysDate);

        return compareNumOfDays;
    }
    
    public boolean olderThan(Person compared) {
        // compare the ages based on birthdays
        if (this.birthday.earlier(compared.birthday)) {          //had to look this up, very difficult at 2am!
            return true;
        } else {
            return false;
        }
    }
    
    public String getName() {
        return this.name;
    }
    
    public String toString() {
        return this.name + ", born " + this.birthday;
    }


}
