START

    // Хэрэглэгчээс хаягийн хэсгүүдийг асууж авах
    PRINT "Улсаа оруулна уу:"
    INPUT улс
    
    PRINT "Аймаг/Мужийг оруулна уу:"
    INPUT аймаг_муж
    
    PRINT "Хот/Дүүргийг оруулна уу:"
    INPUT хот_дүүрэг
    
    PRINT "Гудамжны нэр оруулна уу:"
    INPUT гудамж_нэр
    
    PRINT "Байр/Тайлангийн дугаар оруулна уу:"
    INPUT байр_дугаар
    
    PRINT "Шуудангийн код оруулна уу:"
    INPUT шуудан_код
    
    // Хаягийн бүтцийг шалгах
    IF NOT isValidCountry(улс) THEN
        PRINT "Улс зөв биш байна. Дахин оролдоно уу."
        STOP
    END IF
    
    IF NOT isValidProvince(аймаг_муж) THEN
        PRINT "Аймаг/Муж зөв биш байна. Дахин оролдоно уу."
        STOP
    END IF
    
    IF NOT isValidCity(хот_дүүрэг) THEN
        PRINT "Хот/Дүүрэг зөв биш байна. Дахин оролдоно уу."
        STOP
    END IF
    
    IF NOT isValidStreet(гудамж)
