---
description: Använd sidan Företag i Audience Manager Admin för att skapa ett nytt företag.
seo-description: Använd sidan Företag i Audience Manager Admin för att skapa ett nytt företag.
seo-title: Skapa en företagsprofil
title: Skapa en företagsprofil
uuid: 55de18f8-883d-43fe-b37f-e8805bb92f7a
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# Skapa en företagsprofil {#create-a-company-profile}

Använd [!UICONTROL Companies] sidan i Audience Manager Admin för att skapa ett nytt företag.

<!-- t_create_company.xml -->

>[!NOTE]
>
>Du måste ha rollen för **[!UICONTROL DEXADMIN]** att kunna skapa nya företag.

1. Klicka på **[!UICONTROL Companies]** > **[!UICONTROL Add Company]**.
1. Fyll i fälten:

   * **[!UICONTROL Name]**: (Obligatoriskt) Ange företagets namn.
   * **[!UICONTROL Description]**: (Obligatoriskt) Ange beskrivande information om företaget, till exempel bransch eller dess fullständiga namn.
   * **[!UICONTROL Subdomain]**: (Obligatoriskt) Ange företagets underdomän. Den text du anger är den som visas som underdomän till händelseanropet. Det här kan inte ändras. Det måste vara en sträng med [!DNL URL]giltiga tecken.

      Om ditt företag till exempel har ett namn [!DNL AcmeCorp]blir underdomänen [!DNL acmecorp].

      Audience Manager använder underdomänen för [!UICONTROL Data Collection Server]([!UICONTROL DCS]). I det föregående exemplet, om ditt företag är fullt [!DNL URL] i [!UICONTROL DCS] blir det [!DNL acmecorp.demdex.net].

   * **[!UICONTROL Lifecyle]**: Ange önskat stadium för företaget:
      * **[!UICONTROL Active]**: Ange att företaget ska vara en aktiv Audience Manager-klient. Ett [!UICONTROL Active] konto innebär en betalande kund, inte bara för konsulttjänster, utan även för Audience Manager SKU.
      * **[!UICONTROL Demo]**: Ange att företaget endast är för demoändamål. Rapporteringsdata förfalskas automatiskt.
      * **[!UICONTROL Prospect]**: Ange att företaget är en potentiell Audience Manager-klient, till exempel ett företag som får ett kostnadsfritt [!DNL POC] eller en kontoinställning för en försäljningsdemo.
      * **[!UICONTROL Test]**: Ange att företaget endast ska användas för intern testning.
   * **[!UICONTROL Account Types]**: Ange den fullständiga uppsättningen kontotyper för det här företaget. Ingen kontotyp utesluter varandra med andra typer.
      * **[!UICONTROL Full AAM]**: Ange att företaget ska ha ett fullständigt Adobe Audience Manager-konto och att användarna ska ha inloggningsåtkomst.
      * **[!UICONTROL MMP]**: Ange att företaget har aktiverats för att använda [!UICONTROL Master Marketing Profile] ([!UICONTROL MMP])-funktionerna. Med [!UICONTROL MMP] det kan målgrupper delas över hela Experience Cloud med hjälp av en [!UICONTROL Experience Cloud ID] ([!DNL MCID]) som tilldelats alla besökare och sedan används av Audience Manager. Om du väljer den här kontotypen väljs även kontotypen automatiskt [!UICONTROL Experience Cloud ID Service] .

         Mer information finns i [Målgruppstjänster - Huvudprofil](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)för marknadsföring.
   * **[!UICONTROL Data Source]**: Ange att företaget är en tredjepartsleverantör av data i Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Ange att företaget fungerar som en målinriktningsplattform för kunder med Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Ange att företaget har aktiverats för att använda [!UICONTROL Experience Cloud Visitor ID Service].

      Det [!UICONTROL Experience Cloud Visitor ID Service] ger ett universellt besökar-ID för alla Experience Cloud-lösningar. Mer information finns i användarhandboken för [Experience Cloud Visitor ID-tjänsten](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

   * **[!UICONTROL Agency]**: Ange att företaget ska ha ett [!UICONTROL Agency] konto.



1. Klicka på **[!UICONTROL Create]**. Fortsätt med instruktionerna i [Redigera en företagsprofil](../companies/admin-manage-company-profiles.md#edit-company-profile).

   ![Stegresultat](assets/add_company.png)

## Redigera en företagsprofil {#edit-company-profile}

Redigera ett företags profil, inklusive namn, beskrivning, underdomän, livscykel med mera.

<!-- t_edit_company_profile.xml -->

1. Klicka **[!UICONTROL Companies]** och sedan på önskat företag för att visa dess [!UICONTROL Profile] sida.

   Använd [!UICONTROL Search] rutan eller sidnumreringskontrollerna längst ned i listan för att hitta önskat företag. Du kan sortera varje kolumn i stigande eller fallande ordning genom att klicka på den önskade kolumnens rubrik.

   ![Stegresultat](assets/profile_company.png)

1. Redigera fälten efter behov:

   * **[!UICONTROL Name]**: Redigera företagets namn. Detta är ett obligatoriskt fält.
   * **[!UICONTROL Description]**: Redigera företagsbeskrivningen. Detta är ett obligatoriskt fält.
   * **[!UICONTROL Subdomain]**: (Obligatoriskt) Ange företagets underdomän. Den text du anger är den som visas som underdomän till händelseanropet. Det här kan inte ändras. Det måste vara en sträng med [!DNL URL]giltiga tecken.

      Om ditt företag till exempel har ett namn [!DNL AcmeCorp]blir underdomänen [!DNL acmecorp].

      Audience Manager använder underdomänen för [!UICONTROL Data Collection Server] ([!UICONTROL DCS]). I det föregående exemplet, om ditt företag är fullt [!DNL URL] i [!UICONTROL DCS] blir det [!DNL acmecorp.demdex.net].

   * **[!UICONTROL imsOrgld]**: ([!UICONTROL Identity Management System Organization ID]) Med detta ID kan du ansluta ditt företag till Adobe Experience Cloud.
   * **[!UICONTROL Lifecyle]**: Ange önskat stadium för företaget:
      * **[!UICONTROL Active]**: Ange att företaget ska vara en aktiv Audience Manager-klient. Ett aktivt konto innebär en betalande kund, inte bara för konsulttjänster, utan även för Audience Manager SKU.
      * **[!UICONTROL Demo]**: Ange att företaget endast är för demoändamål. Rapporteringsdata förfalskas automatiskt.
      * **[!UICONTROL Prospect]**: Ange att företaget är en potentiell Audience Manager-klient, till exempel ett företag som får ett kostnadsfritt [!DNL POC] eller en kontoinställning för en försäljningsdemo.
      * **[!UICONTROL Test]**: Ange att företaget endast ska användas för intern testning.
   * **[!UICONTROL Account Types]**: Ange den fullständiga uppsättningen kontotyper för det här företaget. Ingen kontotyp utesluter varandra med andra typer.
      * **[!UICONTROL Full AAM]**: Ange att företaget ska ha ett fullständigt Adobe Audience Manager-konto och att användarna ska ha inloggningsåtkomst.
      * **[!UICONTROL MMP]**: Ange att företaget har aktiverats för att använda funktionerna för masterprofilen ([!UICONTROL MMP]).

         Om du väljer den här kontotypen väljs även den automatiskt **[!UICONTROL Visitor ID Service]** .
Mer information finns i [Målgruppstjänster - Huvudprofil](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html)för marknadsföring.
   * **[!UICONTROL Data Source]**: Ange att företaget är en tredjepartsleverantör av data i Audience Manager.
   * **[!UICONTROL Targeting Partner]**: Ange att företaget fungerar som en målinriktningsplattform för kunder med Audience Manager.
   * **[!UICONTROL Visitor ID Service]**: Ange att företaget har aktiverats för att använda Experience Cloud Visitor ID-tjänsten.

      Experience Cloud Visitor ID-tjänsten tillhandahåller ett universellt besökar-ID för alla Experience Cloud-lösningar. Mer information finns i användarhandboken för [Experience Cloud Visitor ID-tjänsten](https://microsite.omniture.com/t2/help/en_US/mcvid/mcvid_service.html).

   * **[!UICONTROL Agency]**: Ange att företaget ska ha ett byråns konto.
   * **[!UICONTROL Features]**: Välj önskade alternativ:
      * **[!UICONTROL Password Expiration]**: Anger att alla användarlösenord inom det här företaget upphör att gälla efter 90 dagar för att öka säkerheten i Audience Manager.
      * **[!UICONTROL Reporting]**: Aktiverar Audience Manager-rapportering för det här företaget.
      * **[!UICONTROL Role Based Access Controls]**: Aktivera rollbaserade åtkomstkontroller för det här företaget. Med rollbaserade åtkomstkontroller kan du skapa användargrupper med olika åtkomstbehörigheter. Enskilda användare i dessa grupper kan sedan bara få åtkomst till specifika funktioner i Audience Manager.


1. Klicka på **[!UICONTROL Submit Updates]**.

## Ta bort en företagsprofil {#delete-company-profile}

Använd sidan [!UICONTROL Companies] i Audience Manager- [!UICONTROL Admin] verktyget för att ta bort ett befintligt företag.

<!-- t_delete_company.xml -->

>[!NOTE]
>
>Du måste ha rollen för [!UICONTROL DEXADMIN] att kunna ta bort befintliga företag.

1. Om du vill ta bort ett befintligt företag klickar du på **[!UICONTROL Companies]**.

   ![Stegresultat](assets/companies.png)

1. Klicka ![](assets/icon_delete.png) i **[!UICONTROL Actions]** kolumnen för det önskade företaget.
1. Klicka **[!UICONTROL OK]** för att bekräfta borttagningen.