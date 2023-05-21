---
description: Exempel på några vanliga HTTP-makrokombinationer.
seo-description: Examples of some commonly used HTTP macro combinations.
seo-title: HTTP Format Macro Examples
title: Exempel på HTTP-formatmakro
uuid: a81a2e2a-de7e-4b6a-8771-fcfa0dc74570
exl-id: 1f8ccbf3-241d-4bd9-8c35-cf68b12d2713
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 12%

---

# Exempel på HTTP-formatmakro {#http-format-macro-examples}

Exempel på några vanliga användningsområden [!DNL HTTP] makrokombinationer.

Se [HTTP-formatmakron](../formats/web-formats.md) om du vill se en lista över makron och deras definitioner.

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Makroexempel </th> 
   <th colname="col2" class="entry"> Utdataformat </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST; separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|count:&lt;NUM_USERS&gt;|users:[&lt;USER_LIST:{user|&lt;user.aamUuid&gt;:&lt;user.dpUuid&gt;}; separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>"pid_alias|count:2|users:[uuid1:dpuuid1, uuid2:dpuuid2]"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_AGENT&gt;|&lt;IP&gt;|&lt;TIMESTAMP&gt;|&lt;RANDOM&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_LIST:{u|&lt;u.userAgent&gt;|&lt;u.ip&gt;|&lt;u.timestamp&gt;|&lt;u.random&gt;}; separator=", "&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;DP_UUIDS.1&gt; AND &lt;DP_UUIDS.2&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid1 AND dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>users:[&lt;USER_LIST:{user|&lt;user.dpUuids.1&gt; AND &lt;user.dpUuids.2&gt;}; separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>users:[dpuuid1 AND dpuuid2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_known_string=loremlipsum&amp;segid=&lt;TRAITALIAS_LIST; separator=","&gt;&amp;test_dpuuid_1000=&lt;DP_UUIDS.1000&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_known_string=loremlipsum&amp;segid=trait_1,trait_2&amp;test_dpuuid_1000=dpuuid_1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_dpuuids=&lt;DP_UUIDS.(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_dpuuids=dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>"&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST; separator=","&gt;|&lt;REMOVED_TRAITALIAS_LIST; separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"Users":&nbsp;[&lt;USER_LIST:{user|&lt;OPEN_BRACKET&gt; 
      &nbsp;&nbsp;&nbsp;"AAM_UUID":&nbsp;"&lt;user.aamUuid&gt;", 
      &nbsp;&nbsp;&nbsp;"DataPartner_UUID":&nbsp;"&lt;user.dpUuid&gt;", 
      &nbsp;&nbsp;&nbsp;"Segments":&nbsp;[&lt;user.segments:{seg|&lt;OPEN_BRACKET&gt;"Segment":&nbsp;"&lt;seg.traitAlias&gt;"&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;] 
      &nbsp;&nbsp;&nbsp;"Removed_Segments":&nbsp;[&lt;user.removedSegments:{rseg|&lt;OPEN_BRACKET&gt;"Segment":&nbsp;"&lt;rseg.traitAlias&gt;"&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;] 
      &nbsp;&nbsp;&nbsp;&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;]} 
     </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       {&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;"Users":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"AAM_UUID":"uuid1", 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"DataPartner_UUID":"dpuuid1", 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segments":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}, 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias2" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;], 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Removed_Segments":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias3" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}, 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias4" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;] 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;] 
      } 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"Users":&nbsp;[&lt;USER_LIST:{user|&lt;OPEN_BRACKET&gt; 
      &nbsp;&nbsp;&nbsp;"AAM_UUID":&nbsp;"&lt;user.aamUuid&gt;", 
      &nbsp;&nbsp;&nbsp;"DataPartner_UUID":&nbsp;"&lt;user.dpUuid&gt;", 
      &nbsp;&nbsp;&nbsp;"Segments":&nbsp;[&lt;user.segments:{seg|&lt;OPEN_BRACKET&gt;"Segment":&nbsp;"&lt;seg.traitAlias&gt;","Status":&nbsp;"&lt;seg.status&gt;"&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;] 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;CLOSE_BRACKET&gt;};&nbsp;separator=","&gt;]} 
     </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       {&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;"Users":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"AAM_UUID":"uuid1", 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"DataPartner_UUID":"dpuuid1", 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segments":[&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Status":"1" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}, 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;&nbsp; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Segment":"alias2" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"Status":"0" 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;] 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} 
      &nbsp;&nbsp;&nbsp;] 
      } 
     </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;SEGMENTS:{seg|&lt;seg.traitAlias&gt;}; separator=\",\"&gt;|&lt;REMOVED_SEGMENTS:{seg|&lt;seg.traitAlias&gt;}; separator=\",\"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;if(user.segments &amp;&amp; user.removedSegments)&gt;&lt;COMMA&gt;&lt;endif&gt;</code> </p> </td> 
   <td colname="col2"> <p>Skriver ut ett kommatecken om fälten <code>segments</code> och <code>removedSegments</code> är inte tomma. Det här villkorliga uttrycket kan användas för POST-förfrågningar när listor för segment och borttagna segment sammanfogas. </p> </td> 
  </tr> 
 </tbody> 
</table>
