# [ Get Started with Apex Unit Tests](https://trailhead.salesforce.com/content/learn/modules/apex_testing/apex_testing_intro?trailmix_creator_id=trailblazerconnect&trailmix_slug=salesforce-developer-catalyst)

## Problem Statement

![Image](https://github.com/DeependraParichha1004/Trailhead-Solutions/blob/main/Img/apex_testing_1.PNG)

## Code

```
@isTest
private class TestVerifyDate {
    @isTest static void verifyCheck(){
        Date date1 = Date.today();
        Date date2 = date1.addDays(10);
        Date verifydate = VerifyDate.CheckDates(date1,date2);
        System.assertEquals(date2, verifydate);
    }
    @isTest static void verifyCheck2(){
        Date date1 = Date.today();
        Integer totalDays = Date.daysInMonth(date1.year(), date1.month());
		Date lastDay = Date.newInstance(date1.year(), date1.month(), totalDays);
        Date date2 = date1.addDays(35);
        Date verifydate = VerifyDate.CheckDates(date1,date2);
        System.assertEquals(lastDay, verifydate);

    }
    
}


