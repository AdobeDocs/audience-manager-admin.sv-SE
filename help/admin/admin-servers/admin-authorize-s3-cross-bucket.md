---
description: Vissa kunder kanske inte vill ge sina Amazon Simple Storage Service (Amazon S3) åtkomst eller hemliga nycklar till Adobe för att godkänna överföring av måldata till sina bukomater.
seo-description: Vissa kunder kanske inte vill ge sina Amazon Simple Storage Service (Amazon S3) åtkomst eller hemliga nycklar till Adobe för att godkänna överföring av måldata till sina bukomater.
seo-title: Så här auktoriserar du åtkomst till Amazon S3 Bucket för flera konton för batchdestinationer
title: Så här auktoriserar du åtkomst till Amazon S3 Bucket för flera konton för batchdestinationer
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# Så här auktoriserar du åtkomst till Amazon S3 Bucket för flera konton för batchdestinationer{#authorize-cross-account-bucket-batch}

Vissa kunder kanske inte vill ge sina [!DNL Amazon S3] nycklar eller hemliga nycklar till Adobe för att godkänna överföring av måldata till sina bukomater.

Ett alternativ som vi kan erbjuda våra kunder är [!UICONTROL Cross-Account Bucket Permissions] inom [!DNL Amazon S3]. Den här processen beskrivs i [AWS-dokumentationen](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Följ stegen nedan för att aktivera det här alternativet i Audience Manager:

1. Gå till **[!UICONTROL Servers]** och markera **[!UICONTROL Create Server]**.
1. Markera **[!UICONTROL S3]** i den **[!UICONTROL Protocol/Credentials]** nedrullningsbara masken.
1. Markera **[!UICONTROL Use Internal Adobe Key]** alternativet.
1. Använd kundens konto och bucket-namn i [!DNL Amazon S3].
1. Se till att kunden anger kontot [!DNL Amazon S3] på sin `975822914085` [!DNL S3] bucket.

>[!NOTE]
>
>Vår utgivare ser till att behörighetsnivån `bucket-owner-full-control` anges för överförda data, så att kunden kan äga dessa data.