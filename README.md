# -_package com.company;
import javax.swing.*;
import java.time.LocalDate;
import java.time.LocalDateTime;

public class User {
    private LocalDate birthday;
    private LocalDateTime creationDateTime;
    private String name;
    private String surname;
    private String email;
    private String password;

    User(){
        this.creationDateTime = LocalDateTime.now();
    }
    public  void  setBirthday(LocalDate birthday) {
        if (birthday.isBefore ( LocalDate.now ( ) ))
            this.birthday = birthday;
        else
            System.err.println ( "Ошибка даты" );

    }
    public  LocalDate getBirthday (){

        return  this.birthday;
    }
    public  LocalDateTime getCreationDateTime  (){
        return this.creationDateTime;
    }
}
