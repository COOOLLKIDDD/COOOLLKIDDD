<!DOCTYPE html>
<html>
<head>
    <title>Zodiac Sign Finder</title>
</head>
<body>
    <h1>Zodiac Sign Finder</h1>
    <p>Enter your birthdate below to find out your zodiac sign:</p>
    <form>
        <label for="month">Month:</label><br>
        <input type="text" id="month" name="month"><br>
        <label for="day">Day:</label><br>
        <input type="text" id="day" name="day"><br><br>
        <input type="submit" value="Submit">
    </form> 

    <script>
        // get the form and add an event listener
        const form = document.querySelector('form');
        form.addEventListener('submit', e => {
            // prevent the default form submission
            e.preventDefault();

            // get the values of the month and day inputs
            const month = form.month.value;
            const day = form.day.value;

            // determine the user's zodiac sign based on their birthdate
            let zodiacSign = "";
            if ((month == 3 && day >= 21) || (month == 4 && day <= 19)) {
                zodiacSign = "Aries";
            } else if ((month == 4 && day >= 20) || (month == 5 && day <= 20)) {
                zodiacSign = "Taurus";
            } else if ((month == 5 && day >= 21) || (month == 6 && day <= 20)) {
                zodiacSign = "Gemini";
            } else if ((month == 6 && day >= 21) || (month == 7 && day <= 22)) {
                zodiacSign = "Cancer";
            } else if ((month == 7 && day >= 23) || (month == 8 && day <= 22)) {
                zodiacSign = "Leo";
            } else if ((month == 8 && day >= 23) || (month == 9 && day <= 22)) {
                zodiacSign = "Virgo";
            } else if ((month == 9 && day >= 23) || (month == 10 && day <= 22)) {
                zodiacSign = "Libra";
            } else if ((month == 10 && day >= 23) || (month == 11 && day <= 21)) {
                zodiacSign = "Scorpio";
            } else if ((month == 11 && day >= 22) || (month == 12 && day <= 21)) {
                zodiacSign = "Sagittarius";
            } else if ((month == 12 && day >= 22) || (month == 1 && day <= 19)) {
                zodiacSign = "Capricorn";
            } else if ((month == 1 && day >= 20) || (month == 2 && day <= 18)) {
                zodiacSign = "Aquarius";
            } else if ((month == 2 && day >= 19) || (month == 3 && day <= 20)) {
                zodiacSign = "Pisces";
            }

            // display the user's zodiac sign
            const result = document.createElement('p');
            result.textContent = `Your zodiac sign
