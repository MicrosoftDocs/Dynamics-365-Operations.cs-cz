---
title: "Schválení faktury mobilních"
description: "Mobilní funkce v Microsoft Dynamics 365 pro operace může uživatel obchodní návrh mobilní zkušenosti. Pro pokročilé scénáře platformu také Řekněme vývojáři rozšířit možnosti jak nadcházejících událostech. Nejúčinnějším způsobem naučit některé nové pojmy v mobile je projít proces navrhování několik scénářů. Toto téma je určen k poskytování praktického přístupu k navrhování mobilních scénářů převzetím dodavatele schválení faktury pro mobilní telefon jako případu použití. V tomto tématu vám pomohou navrhnout jiné varianty scénářů a lze také použít další scénáře, které nesouvisejí s faktury dodavatele."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Schválení faktury mobilních

[!include[banner](../includes/banner.md)]


Mobilní funkce v Microsoft Dynamics 365 pro operace může uživatel obchodní návrh mobilní zkušenosti. Pro pokročilé scénáře platformu také Řekněme vývojáři rozšířit možnosti jak nadcházejících událostech. Nejúčinnějším způsobem naučit některé nové pojmy v mobile je projít proces navrhování několik scénářů. Toto téma je určen k poskytování praktického přístupu k navrhování mobilních scénářů převzetím dodavatele schválení faktury pro mobilní telefon jako případu použití. V tomto tématu vám pomohou navrhnout jiné varianty scénářů a lze také použít další scénáře, které nesouvisejí s faktury dodavatele.

<a name="prerequisites"></a>Předpoklady
-------------

| Předpoklad                                                                                            | popis                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobilní handbook předem přečíst.                                                                                |(/ dynamics365/operace/dev-itpro/mobilní telefon apps / mobile-platform.md)                                                                                                  |
| Dynamics 365 pro operace                                                                             | Prostředí, které má Microsoft Dynamics 365 pro verzi operace 1611 a Microsoft Dynamics pro operace platformy aktualizace 3 (listopad 2016)                   |
| Instalace opravy hotfix KB 3204341.                                                                              | Záznamník úkolů můžete zaznamenat omylem dva příkazy zavřít dialogová okna rozevírací seznam, který bude obsažen v Dynamics 365 pro operace aktualizace platformy 3 (aktualizace dne 2016) |
| Instalace opravy hotfix KB 3207800.                                                                              | Tato oprava hotfix umožňuje přílohy v mobilní klient, který bude obsažen v Dynamics 365 pro operace aktualizace platformy 3 (aktualizace dne 2016).           |
| Instalace opravy hotfix KB 3208224.                                                                              | Kód aplikace pro použití schválení faktury dodavatele mobilních to je zahrnuta v aplikaci Microsoft Dynamics AX 7.0.1 (květen 2016).                          |
| Android nebo iOS nebo zařízení systému Windows, který má mobilní aplikace nainstalována Dynamics 365 pro operace | Vyhledat aplikace v úložišti příslušné aplikace.                                                                                                                     |

## <a name="introduction"></a>Úvod
Mobilní schválení faktur dodavatele vyžadují tři opravy hotfix, které jsou uvedeny v části "Předpoklady". Tyto opravy hotfix nepřinesou pracovní prostor pro schválení faktury. Chcete-li zjistit, co je pracovní prostor v souvislosti s mobilní, číst mobilní příručka, která je uvedena v části "Předpoklady". V pracovním prostoru schválení faktury musí být řešeny. 

Každá organizace orchestrates a jiným způsobem definuje svůj obchodní proces pro faktury dodavatele. Dříve, než vytvoříte mobilní prostředí pro schválení faktury dodavatele, měli byste zvážit následující aspekty obchodního procesu. Myšlenka je použití těchto datových bodů co nejvíce k optimalizování uživatelského prostředí v zařízení.

-   Která pole z hlavičky faktury uživatel chtít vidět do mobilního prostředí a v jakém pořadí?
-   Která pole z řádků fakturace uživatel chtít vidět do mobilního prostředí a v jakém pořadí?
-   Kolik řádků faktury jsou ve faktuře? Platí zde pravidlo 80-20 a optimalizovat 80procent $2.
-   Budou uživatelé chtějí vidět rozúčtování (kódování faktury) v mobilním zařízení během recenze? Pokud je odpověď na tuto otázku Ano, zvažte následující otázky:
    -   Kolik rozúčtování (rozšířená cena, DPH, poplatky, rozdělení atd.) jsou pro řádek faktury? Znovu použít pravidlo 80-20.
    -   Faktury také mají rozúčtování v hlavičce faktury? V takovém případě by tyto rozúčtování k dispozici v zařízení?

> [!NOTE]
> Toto téma není vysvětlují, jak upravit rozúčtování, protože tato funkce není aktuálně podporována pro mobilní scénáře.

-   Budou uživatelé chtějí vidět přílohy pro fakturu na zařízení?

Návrh mobilního prostředí schválení faktury se liší v závislosti na odpovědi na tyto otázky. Cílem je optimalizovat uživatelské prostředí pro obchodní proces Mobile v organizaci. Ve zbývající části tohoto tématu se podíváme na dvě varianty scénáře, které jsou založeny na různé odpovědi na předchozí dotazy. 

Jako obecné vodítko, při práci s návrhářem mobilní Ujistěte se, chcete-li publikovat změny, aby se zabránilo ztrátě aktualizací.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Návrh scénáře schválení jednoduché faktury pro společnosti Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atribut scénáře</th>
<th>Odpověď</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Která pole z hlavičky faktury uživatel chtít vidět do mobilního prostředí a v jakém pořadí?</td>
<td><ol>
<li>Název dodavatele</li>
<li>Faktura celkem</li>
<li>Účet faktury</li>
<li>Číslo faktury</li>
<li>Datum fakturace</li>
<li>Popis faktury</li>
<li>Datum splatnosti</li>
<li>Měna faktury</li>
</ol></td>
</tr>
<tr class="even">
<td>Která pole z řádků fakturace uživatel chtít vidět do mobilního prostředí a v jakém pořadí?</td>
<td><ol>
<li>Kategorie zásobování</li>
<li>Množství</li>
<li>Jedn. cena</li>
<li>Čistá částka řádku</li>
<li>Částka sestavy 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kolik řádků faktury jsou ve faktuře? Platí zde pravidlo 80-20 a optimalizovat 80procent $2.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Budou uživatelé chtějí vidět rozúčtování (kódování faktury) v mobilním zařízení během recenze?</td>
<td>Ano</td>
</tr>
<tr class="odd">
<td>Kolik rozúčtování (rozšířená cena, DPH, poplatky atd.) jsou pro řádek faktury? Znovu použít pravidlo 80-20.</td>
<td>Rozšířená cena: DPH 2: poplatky 0: 0</td>
</tr>
<tr class="even">
<td>Faktury také mají rozúčtování v hlavičce faktury? V takovém případě by tyto rozúčtování k dispozici v zařízení?</td>
<td>Nepoužito</td>
</tr>
<tr class="odd">
<td>Budou uživatelé chtějí vidět přílohy pro fakturu na zařízení?</td>
<td>Ano</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Vytvoření pracovního prostoru

1.  V prohlížeči otevřete 365 Dynamics pro operace a přihlaste se.
2.  Poté, co jste přihlášeni, připojit **& režim = mobilní** na adresu URL, jak je znázorněno v následujícím příkladu a aktualizace stránky: https://&lt;yoururl&gt;/? cmp = usmf & mi = DefaultDashboard**& režim = mobilní**
3.  Klepněte **nastavení** (zařízení) tlačítko v pravém horním rohu stránky a poté klepněte na **mobilní aplikace**. Mobilní aplikace Návrhář musí zobrazí stejně jako úkol záznam se zobrazí.
4.  Klepněte na tlačítko **přidat** Chcete-li vytvořit nový pracovní prostor. V tomto příkladu název pracovního prostoru **schválení**.
5.  Zadejte popis.
6.  Vyberte barvu prostoru. Barevný prostor bude použit pro celkový styl mobilního prostředí pro tento pracovní prostor.
7.  Vyberte ikonu pro pracovní prostor.
8.  Klepněte na **v**
9.  Klepněte na tlačítko **publikovat pracovního prostoru** uložit změny

### <a name="vendor-invoices-assigned-to-me"></a>Faktury dodavatele přiřazené mně

První mobilní stránka, která by měla navrhnout je seznam faktur, které jsou přiřazeny uživatelům na revizi. Navrhnout tuto stránku mobilní, použít **VendMobileInvoiceAssignedToMeListPage** stránku 365 Dynamics pro operace. Před provedením tohoto postupu, ujistěte se, že alespoň jeden dodavatelské faktury je přiřazen k recenzi, a má dva rozdělení řádku faktury. Toto nastavení splňuje požadavky pro tento scénář.

1.  V 365 Dynamics pro adresu URL operace, nahraďte název položky nabídky s **VendMobileInvoiceAssignedToMeListPage** otevřete mobilní verzi **nevyřízené faktury dodavatele přiřazené mně** stránku seznamu **závazků** modulu. V závislosti na počtu faktur, které jste ve vašem systému přiřadili jste na této stránce se zobrazí tyto faktury. Chcete-li najít konkrétní fakturu, můžete použít filtr na levé straně. Jsme však nevyžadují, aby konkrétní fakturu pro tento příklad. Vyžadujeme pouze některé faktury přiřazen, která bude umožňují navrhnout stránku mobilní. Nové stránky, které jsou k dispozici byly navrženy speciálně pro vývoj mobilních scénářů pro faktury dodavatele. Proto je nutné použít tyto stránky. Adresa URL by se měla podobat následující adresu URL a po jeho zadání, musí být uvedeny na stránce, která je znázorněno na obrázku: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& režim = mobilní [![stránku nevyřízené faktury dodavatele přiřazené mně](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Klepněte **nastavení** (zařízení) tlačítko v pravém horním rohu stránky a poté klepněte na **mobilní aplikace**
3.  Vyberte pracovní prostor a klikněte na **úpravy**
4.  Klepněte na tlačítko **stránku přidat** vytvořte první stránku mobilní.
5.  Zadejte název, jako například **Moje faktury dodavatele**a popis, jako například **faktury dodavatele přiřazené mně k recenzi**.
6.  Click **Done**.
7.  V Návrháři mobilní na **pole** karta, klepněte na tlačítko **vyberte pole**. Sloupce na stránce seznamu musí vypadat podobně jako na následujícím obrázku. [![Sloupců nevyřízené faktury dodavatele přiřazené mně stránky](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Přidejte požadované sloupce na stránce seznamu, musí být uvedeny pro uživatele na mobilní stránce. Pořadí, ve kterém můžete přidat je pořadí, ve kterém se pole zobrazí koncovému uživateli. Jediný způsob, jak změnit pořadí polí, budou znovu vyberte všechna pole. Na základě požadavků pro tento scénář, jsou vyžadovány následující osmi polí. Nicméně někteří uživatelé zvážit osmi polí příliš mnoho informací v mobilním zařízení. Nejdůležitější pole proto ukážeme mobilního seznamu zobrazení. Zbývající pole se zobrazí v zobrazení Podrobnosti, které můžeme navrhnout později. Nyní přidáme následující pole. Klepněte na znaménko plus (**+**) v těchto sloupcích, chcete-li přidat na stránku mobilní.
    1.  Název dodavatele
    2.  Faktura celkem
    3.  Účet faktury
    4.  Číslo faktury
    5.  Datum fakturace

    Po přidání pole, mobilní stránky, vypadat podobně jako na následujícím obrázku. [![Stránka po přidání polí](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Následující sloupce musí také přidat nyní, takže jsme později povolit akce pracovního postupu.
    1.  Zobrazit dokončit úkol
    2.  Zobrazit delegovat úkol
    3.  Zobrazit úkol odvolání
    4.  Zobrazit úkol odmítnout
    5.  Zobrazit požadavek na dokončení úkolu
    6.  Zobrazit úlohu opětovného odeslání

10. Klepněte na **v** Chcete-li ukončit režim úprav.
11. Klepněte na tlačítko **zpět** a **v** ukončení pracovního prostoru
12. Klepněte na tlačítko **publikovat pracovního prostoru** uložit práci.
13. Povolit **seznam faktur Zobrazit fakturu na celkovou nevyřízené dodavatele** ve formuláři Parametry závazků podle **fakturace**. Všimněte si, že pouze tím, že tento parametr součty faktury bude vypočtena zobrazený na stránce seznamu faktur dodavatele čekající na vyřízení. Toto je nová funkce v rámci předem nezbytná oprava hotfix 3208224.

### <a name="vendor-invoice-details"></a>Podrobnosti faktury dodavatele

Navrhovat stránky podrobnosti faktury pro mobilní telefon, použijte **VendMobileInvoiceHeaderDetails** stránku 365 Dynamics pro operace. Všimněte si, že v závislosti na počtu faktur, které máte ve vašem systému, tato stránka zobrazuje nejstarší faktury (faktura, která byla vytvořena jako první). Chcete-li najít konkrétní fakturu, můžete použít filtr na levé straně. Jsme však nevyžadují, aby konkrétní fakturu pro tento příklad. Vyžadujeme pouze některá data faktury tak, že můžeme navrhnout stránku mobilní. [![Pracovní postup](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  V 365 Dynamics pro adresu URL operace, nahraďte název položky nabídky s **VendMobileInvoiceHeaderDetails** k otevření formuláře
2.  Otevřete Mobilní návrhář z **nastavení** tlačítko (zařízení).
3.  Klepněte **úprava** tlačítka spusťte režim úprav v pracovním prostoru.
4.  Vyberte ** Moje faktury dodavatele ** stránky, kterou jste dříve vytvořili a potom klepněte na tlačítko **úprava**.
5.  Na **pole** karta, klepněte **mřížka** záhlaví sloupce.
6.  Klepněte na tlačítko **vlastnosti**&gt;**stránku přidat**. **Poznámka:** po klepnutí **mřížka** čísla a přidat na stránku Podrobnosti stránka je automaticky navázán vztah.
7.  Zadejte název stránky, například **detaily faktury**a popis, jako například **zobrazení záhlaví faktury a podrobnosti řádku**.
8.  Klepněte na tlačítko **vyberte pole**. Všimněte si, že pořadí, ve kterém můžete přidat je pořadí, ve kterém se pole zobrazí koncovému uživateli. Jediný způsob, jak změnit pořadí polí, budou znovu vyberte všechna pole.
9.  Přidejte následující pole v záhlaví na základě požadavků pro tento scénář:
    1.  Název dodavatele
    2.  Faktura celkem
    3.  Účet faktury
    4.  Číslo faktury
    5.  Datum fakturace
    6.  Popis faktury
    7.  Datum splatnosti
    8.  Měna faktury

10. Z řádků mřížky na stránce přidejte následující pole:
    1.  Kategorie zásobování
    2.  Množství
    3.  Jedn. cena
    4.  Čistá částka řádku
    5.  Částka sestavy 1099

11. Po přidání všech polí z předchozích dvou kroků, klepněte na **v**. Stránka musí vypadat podobně jako na následujícím obrázku. [![Stránka po přidání polí](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Klepněte na **v** Chcete-li ukončit režim úprav.
13. Klepněte na tlačítko **zpět** a **v** ukončení pracovního prostoru
14. Klepněte na tlačítko **publikovat pracovního prostoru** uložit práci

### <a name="workflow-actions"></a>Akce workflowu

Chcete-li přidat akce pracovního postupu, použijte **VendMobileInvoiceHeaderDetails** stránku 365 Dynamics pro operace. Chcete-li tuto stránku otevřít, nahraďte název položky nabídky v adrese URL, stejně jako dříve. Potom otevřete Mobilní návrhář z **nastavení** tlačítko (zařízení). Postupujte takto Chcete-li přidat akce pracovního postupu na stránce Podrobnosti.

1.  Klepněte **úprava** tlačítka spusťte režim úprav v pracovním prostoru.
2.  Vyberte **detaily faktury** stránky, kterou jste dříve vytvořili a potom klepněte na tlačítko **úprava**.
3.  Na **akcí** karta, klepněte na tlačítko **přidat akci**.
4.  Zadejte název akce, jako například **schválit**a popis, jako například **Schválit fakturu**. Všimněte si, že změní název akce, kterou zde zadáte název akce, která se zobrazí uživateli v mobilní aplikace.
5.  Click **Done**.
6.  Klepněte na tlačítko **vyberte pole**.
7.  V procesu pracovního postupu, přejděte **VendMobileInvoiceHeaderDetails** stránku a provést akci, kterou chcete nahrát. Ujistěte se, zadejte komentáře pracovního postupu během tohoto procesu tak, aby pole komentáře je také součástí mobilního prostředí.
8.  Po spuštění akcí pracovního postupu, klepněte na **v** k dokončení úkolu vyberte pole.
9.  Klepněte na **v** Chcete-li ukončit režim úprav.
10. Klepněte na tlačítko **zpět** a **v** ukončení pracovního prostoru
11. Klepněte na tlačítko **publikovat pracovního prostoru** uložit práci
12. Opakujte kroky 3 až 11 k zaznamenání všech akcí pracovního postupu požadováno. Všimněte si, že je povinnost mít faktury přiřazen ve stavu ke zpřístupnění akce pracovního postupu, chcete-li navrhnout pro.
13. Otevřete Poznámkový blok nebo Microsoft Visual Studio a vložte následující kód. Uložte soubor jako soubor JS. Tento kód provádí dvě věci:
    1.  Skryje sloupce extra týkající se pracovního postupu, které jsme přidali dříve na stránce Mobilní seznam. Můžeme přidat tyto sloupce tak, aby aplikace má tyto informace v kontextu a provést další krok.
    2.  Podle kroku pracovního postupu, který je aktivní, použije logiku, chcete-li zobrazit pouze akce.

Všimněte si, že název stránky a další ovládací prvky v JS kódu musí být shodné z pracovního prostoru.

1.  Hlavní funkce (MetadataService, které byly dataService, cacheService, $q) {vrátit {Applnit: funkce (appMetadata) {/ / skrýt ovládací prvky, které musí být přítomny, ale nejsou viditelné metadataService.configureControl ("My--faktury dodavatele, 'ShowAccept' {skryté: PRAVDA}); metadataService.configureControl (" My--faktury dodavatele, "ShowApprove" {skryté: PRAVDA}); metadataService.configureControl ("My--faktury dodavatele,"ShowReject"{skryté: true}); metadataService.configureControl (" My--faktury dodavatele, 'ShowDelegate' {skryté: PRAVDA}); metadataService.configureControl ("My--faktury dodavatele, 'ShowRequestChange' {skryté: PRAVDA}); metadataService.configureControl (" My--faktury dodavatele, "ShowRecall" {skryté: PRAVDA}); metadataService.configureControl ("My--faktury dodavatele,"ShowComplete"{skryté: PRAVDA}); metadataService.configureControl (" My--faktury dodavatele, 'ShowResubmit' { skryté: true}); }, pageInit: funkce (pageMetadata, params) {Pokud (pageMetadata.Name == "Podrobnosti faktury") {/ / akce pracovního postupu zobrazit nebo skrýt podle pracovního postupu krok metadataService.configureAction ("Přijmout", {viditelné: true}); metadataService.configureAction ("Schválit" {viditelné: PRAVDA}); metadataService.configureAction ("Odmítnout", {viditelné: PRAVDA}); metadataService.configureAction ("Delegát" {viditelné: PRAVDA}); metadataService.configureAction ("požádat o změnu", {viditelné: PRAVDA}); metadataService.configureAction ("Odvolání" {viditelné: PRAVDA}); metadataService.configureAction ('Dokončit' {viditelné: true}); metadataService.configureAction (znovu "odešle", {viditelné: true});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Odeslat kód souboru do pracovního prostoru výběrem **logiky** kartu
3.  Klepněte na **v** Chcete-li ukončit režim úprav.
4.  Klepněte na tlačítko **zpět** a **v** ukončení pracovního prostoru
5.  Klepněte na tlačítko **publikovat pracovního prostoru** uložit práci

### <a name="vendor-invoice-attachments"></a>Přílohy pro faktury dodavatele

1.  Klepněte **nastavení** (zařízení) tlačítko v pravém horním rohu stránky a poté klepněte na **mobilní aplikace**
2.  Klepněte **úprava** tlačítka spusťte režim úprav v pracovním prostoru.
3.  Vyberte ** detaily faktury ** stránky, kterou jste dříve vytvořili a potom klepněte na tlačítko **úprava**.
4.  Nastavit **Správa dokumentů** možnost na **Ano** jak je ukázáno níže. **Poznámka:** Pokud neexistují žádné požadavky na mobilním zařízení zobrazit přílohy, můžete nechat tuto možnost nastavte na **č**, což je výchozí nastavení.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Klepněte na **v** Chcete-li ukončit režim úprav.
7.  Klepněte na tlačítko **zpět** a **v** ukončení pracovního prostoru
8.  Klepněte na tlačítko **publikovat pracovního prostoru** uložit práci

### <a name="vendor-invoice-line-distributions"></a>Distribuce pro řádek faktury dodavatele

Požadavky pro tento scénář potvrďte, že bude pouze řádek úrovně distribuce a faktury budou mít vždy pouze jeden řádek. Vzhledem k tomu, že tento scénář je jednoduchý, musí být natolik jednoduché, že uživatel nemá k zobrazení podrobností k zobrazení distribucí několik úrovní uživatelského prostředí na mobilním zařízení. Faktury dodavatele v 365 Dynamics pro operace patří možnost zobrazení všech distribucí z hlavičky faktury. Tyto zkušenosti je potřebujeme pro mobilní scénář. Proto použijeme **VendMobileInvoiceAllDistributionTree** stránku Navrhnout tuto část mobilní scénář. 

> [!NOTE] 
> Znalost požadavků nám rozhodněte, které konkrétní stránky používat a jak přesně optimalizovat mobilního prostředí pro uživatele, když navrhujeme scénář. Ve druhém scénáři použijeme jinou stránku Zobrazit rozúčtování, protože se liší požadavky pro tento scénář.

1.  V adrese URL nahraďte název položky nabídky, stejně jako před. Stránky, které se objeví, měl by vypadat jako na následujícím obrázku. [![Všechny stránky distribucí](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Otevřete Mobilní návrhář z **nastavení** tlačítko (zařízení).
3.  Klepněte **úprava** tlačítka spusťte režim úprav v pracovním prostoru. **Poznámka:**, byly automaticky vytvořeny dvě nové stránky se zobrazí. Systém vytvoří tyto stránky, protože je zapnuta správa dokumentů v předchozí části. Tyto nové stránky můžete ignorovat.
4.  Klepněte na tlačítko **stránku přidat**.
5.  Zadejte název stránky, například **zobrazení účetních**a popis, jako například **zobrazení účtování faktury**.
6.  Click **Done**.
7.  Na **pole** karta, klepněte na tlačítko **vyberte pole**, z rozdělení stránky zaškrtněte následující políčka a potom klepněte na tlačítko **v**:
    1.  Částka
    2.  Měna
    3.  Účet hlavní knihy

> [!NOTE] 
> Jsme nevybrali **popis** sloupec z mřížky distribuce, protože požadavky pro tento scénář potvrdila, že výsledná cena je pouze částku, která bude rozúčtování. Uživatel proto nebude vyžadovat další pole k určení typu částky, který je rozdělení. V dalším scénáři však jsme **bude** tyto informace použít, protože požadavky na tuto situaci, že mají jiné typy částku rozdělení (například DPH).
8.  Klepněte na **v** Chcete-li ukončit režim úprav.
9.  Klepněte na tlačítko **zpět** a **v** ukončení pracovního prostoru
10. Klepněte na tlačítko **publikovat pracovního prostoru** uložit práci

**Poznámka:****zobrazení účetních** mobilní stránku není propojen právě některý z mobilních stránek, které jsme doposud vytvořili. Protože má být uživatel moci přejít na **zobrazení účetních** stránky z **detaily faktury** stránky na mobilním zařízení, musí nabízíme navigaci z **detaily faktury** stránce **zobrazení účetních** stránky. Můžeme navázat tato navigace pomocí další logiku pomocí jazyka JavaScript.

1.  Otevření souboru .js, který jste vytvořili dříve a přidat zvýrazněné řádky v následujícím kódu. Tento kód provádí dvě věci:
    1.  Pomáhá zajistit, že uživatelům nebude umožněno přejít přímo z pracovního prostoru, chcete-li **zobrazení účetních** stránky.
    2.  Zjistí-li ovládací prvek navigace z **detaily faktury** stránce **zobrazení účetních** stránky.

> [!NOTE] 
> Název stránky a další ovládací prvky v JS kódu musí být stejné z pracovního prostoru.

1.  Hlavní funkce (MetadataService, které byly dataService, cacheService, $q) {vrátit {Applnit: funkce (appMetadata) {/ / skrýt ovládací prvky, které musí být přítomny, ale nejsou viditelné metadataService.configureControl ("My--faktury dodavatele, 'ShowAccept' {skryté: PRAVDA}); metadataService.configureControl (" My--faktury dodavatele, "ShowApprove" {skryté: PRAVDA}); metadataService.configureControl ("My--faktury dodavatele,"ShowReject"{skryté: true}); metadataService.configureControl (" My--faktury dodavatele, 'ShowDelegate' {skryté: PRAVDA}); metadataService.configureControl ("My--faktury dodavatele, 'ShowRequestChange' {skryté: PRAVDA}); metadataService.configureControl (" My--faktury dodavatele, "ShowRecall" {skryté: PRAVDA}); metadataService.configureControl ("My--faktury dodavatele,"ShowComplete"{skryté: PRAVDA}); metadataService.configureControl (" My--faktury dodavatele, 'ShowResubmit' { skryté: true}); Skrytí stránek pro kořenový navigační metadataService.hideNavigation('View-accounting'); Odkaz zobrazíte účetní metadataService.addLink ("faktury podrobnosti" účetní zobrazení "," zobrazení účetní nav řízení ","Zobrazení účetní", true); }, pageInit: funkce (pageMetadata, params) {Pokud (pageMetadata.Name == "Podrobnosti faktury") {/ / akce pracovního postupu zobrazit nebo skrýt podle pracovního postupu krok metadataService.configureAction ("Přijmout", {viditelné: true}); metadataService.configureAction ("Schválit" {viditelné: PRAVDA}); metadataService.configureAction ("Odmítnout", {viditelné: PRAVDA}); metadataService.configureAction ("Delegát" {viditelné: PRAVDA}); metadataService.configureAction ("požádat o změnu", {viditelné: PRAVDA}); metadataService.configureAction ("Odvolání" {viditelné: PRAVDA}); metadataService.configureAction ('Dokončit' {viditelné: true}); metadataService.configureAction (znovu "odešle", {viditelné: true});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Odeslat kód souboru do pracovního prostoru výběrem **logiky** kartu přepsat předchozí kód
3.  Klepněte na **v** Chcete-li ukončit režim úprav.
4.  Klepněte na tlačítko **zpět** a **v** ukončení pracovního prostoru
5.  Klepněte na tlačítko **publikovat pracovního prostoru** uložit práci

### <a name="validation"></a>Ověření

Z mobilního zařízení otevřete aplikace a připojit se k vaší Dynamics 365 instance operace. Ujistěte se, přihlásit se do společnosti, kde faktury dodavatele vám byly přiřazeny k revizi. Je třeba provést následující akce:

-   Najdete **schválení** prostoru.
-   Přejít k podrobnostem **schválení** prostoru a viz **Moje faktury dodavatele** stránky.
-   Přejít k podrobnostem **Moje faktury dodavatele** stránku a zobrazit seznam faktur, které vám byly přiřazeny.
-   Jedné z faktur k podrobnostem a zobrazit podrobnosti faktury záhlaví a podrobností řádků.
-   Na stránce Podrobnosti viz odkaz na přílohy a pomocí tohoto odkazu můžete přejít na seznam příloh a přílohy zobrazit.
-   Na stránce Podrobnosti viz odkaz **zobrazení účetních** stránku a pomocí tohoto odkazu můžete přejít na stránku distribuce a zobrazení distribucí.
-   Na stránce Podrobnosti klepněte **akce** nabídky v dolní části a provádět akce pracovního postupu, které jsou použitelné pro krok pracovního postupu.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Návrh scénáře schválení komplexní faktury Fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atribut scénáře</th>
<th>Odpověď</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Která pole z hlavičky faktury uživatel chtít vidět do mobilního prostředí a v jakém pořadí?</td>
<td><ol>
<li>Název dodavatele</li>
<li>Fakturovaná částka</li>
<li>Účet faktury</li>
<li>Číslo faktury</li>
<li>Datum fakturace</li>
<li>Popis faktury</li>
<li>Datum splatnosti</li>
<li>Měna faktury</li>
</ol></td>
</tr>
<tr class="even">
<td>Která pole z řádků fakturace uživatel chtít vidět do mobilního prostředí a v jakém pořadí?</td>
<td><ol>
<li>Kategorie zásobování</li>
<li>Množství</li>
<li>Jedn. cena</li>
<li>Čistá částka řádku</li>
<li>Částka sestavy 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kolik řádků faktury jsou ve faktuře? Platí zde pravidlo 80-20 a optimalizovat 80procent $2.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Budou uživatelé chtějí vidět rozúčtování (kódování faktury) v mobilním zařízení během recenze?</td>
<td>Ano</td>
</tr>
<tr class="odd">
<td>Kolik rozúčtování (rozšířená cena, DPH, poplatky atd.) jsou pro řádek faktury? Znovu použít pravidlo 80-20.</td>
<td>Rozšířená cena: DPH 2: 2 poplatky: 2</td>
</tr>
<tr class="even">
<td>Faktury také mají rozúčtování v hlavičce faktury? V takovém případě by tyto rozúčtování k dispozici v zařízení?</td>
<td>Nepoužito</td>
</tr>
<tr class="odd">
<td>Budou uživatelé chtějí vidět přílohy pro fakturu na zařízení?</td>
<td>Ano</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Cvičení

Tyto změny lze provést pro scénář 1, na základě požadavků pro scénář 2. Tato část slouží jako cvičení, které můžete provést pro studijní účely.

1.  Vzhledem k tomu, že další řádky faktury jsou očekávány v scénář 2, vám pomůže následující změny návrhu optimalizování uživatelského prostředí na mobilním zařízení:
    1.  Místo zobrazení řádků faktury na stránce Podrobnosti (jako v scénář 1), uživatelé mohou zobrazit řádky na samostatnou stránku mobilní.
    2.  Vzhledem k tomu, že v tomto případě se očekává více než jeden řádek faktury, pokud **VendMobileInvoiceAllDistributionTree** stránka slouží k vytvoření stránky distribucí pro mobilní telefon (jako v scénář 1), může být matoucí pro uživatele ke korelaci na rozdělování řádků. Proto použít **VendMobileInvoiceLineDistributionTree** stránku navrhnout rozložení stránky.
    3.  V ideálním případě by rozdělení se mají v rámci řádku faktury v tomto scénáři. Proto se ujistěte, že uživatel můžete přejít k podrobnostem linku najdete na stránce distribuce. Použijte funkci odkaz stránky navázat procházení, stejně jako stránek záhlaví a podrobností v scénář 1.

2.  Vzhledem k tomu, že na rozdělení v scénář 2 (prodejní daně, poplatky a tak dále) se očekává více než jeden typ částky, je užitečné, chcete-li zobrazit popis typu Částka. (Můžeme vynechat tuto informaci v scénář 1).

## <a name="conclusion"></a>Závěr
Mobilní platformy a možnosti aplikace umožňují navrhnout mobilních scénářů, které jsou optimalizovány pro základní organizace uživatele. Na základě příkladů uvedených v tomto tématu, můžete zkusit další varianty a vytvořit různé zkušenosti, které splňují specifické potřeby.




