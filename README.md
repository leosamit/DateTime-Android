##Date Time Library for Android
This library is a extension of ThreeTenABP by JakeWatron


#Formatter

fun LocalDateTime.toIsoLocalDateTimeString(): String
// => 2020-04-21T05:21:13

LocalDateTime.toStringWithPattern(pattern: String): String
//  "dd/MM/yyyy HH:mm:ss",   =>  21/04/2020 05:21:13
//  "dd/MM/yyyy",            =>  21/04/2020
//  "d MMM yyyy",            =>  21 Apr 2020
//  "yyyy-MM-dd",            =>  2020-04-21
//  "MMM dd'`'yy 'at' H:mm", =>  Apr 21'20 at 5:21
//  "EEE, d MMM, h:mm a",    =>  Thu, 21 Apr, 5:21 am
//  "EEE, d MMM",            =>  Thu, 21 Apr
//  "h:mm a",                =>  5:21 am
//  "hh:mm a"                =>  05:21 am

fun Month.fullDisplayName(): String // April
fun Month.shortDisplayName(): String // Apr

#Parser
fun String?.toIsoLocalDateTime(): LocalDateTime?
// "2020-04-21T05:21:13" => LocalDateTime

#Calculator
fun durationInDaysAndHours(from: LocalDateTime, to: LocalDateTime): Pair<Int, Int>
/** Return duration in a format "x days and y hours"*/