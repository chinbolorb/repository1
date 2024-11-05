Хэрэглэгчийн гэрийн хаягийг авах алгоритм нь хэрэглэгчийн өгөгдлийг асууж авах, хэлбэрт оруулах, алдааг шалгах, тохирох хариулт авах зэргийг агуулдаг. Хэрэглэгчийн гэрийн хаяг авахад ихэвчлэн дараах алхмуудыг дагах хэрэгтэй:

### 1. Хэрэглэгчээс гэрийн хаяг авах
Алгоритм нь хэрэглэгчээс хаяг авахын өмнө хэд хэдэн зүйлсийг тодорхойлох шаардлагатай:

- Хаягийн бүрэн бүтэц: Улс, муж/аймаг, хот, дүүрэг, гудамж, байршил гэх мэт.
- Хаяг нь зөв бүтэцтэй байх: Хэрэглэгчийн оруулсан хаяг нь тодорхой хэлбэрт орох ёстой (жишээ нь, гудамжны нэр, байршлын дугаар, шуудангийн код гэх мэт).

### 2. Хэрэглэгчийн хаягийг шалгах
Хэрэглэгчийн хаяг нь зөв бүтэцтэй эсэхийг шалгах хэрэгтэй. Хаягийн бүрдэл хэсэг тус бүрийг шалгах шаардлагатай байдаг (жишээ нь, шуудангийн код 5 оронтой байх, гудамжны нэр зөв бичигдсэн байх гэх мэт).

### 3. Хаягийн өгөгдөл авах
Хэрэглэгчийн хаяг нь хэд хэдэн хэсгээс бүрддэг тул бүх хэсгийг тус тусад нь асуух хэрэгтэй. Эдгээр хэсгүүд нь:
- Улс
- Аймаг/муж
- Хот
- Гудамж
- Байр/Тайлан
- Шуудангийн код

### 4. Алгоритмын бүтэц

```pseudo
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
    
    IF NOT isValidStreet(гудам