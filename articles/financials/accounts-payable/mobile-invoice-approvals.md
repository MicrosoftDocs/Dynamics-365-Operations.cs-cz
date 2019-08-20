---
title: Mobilní schvalování faktur
description: Toto téma poskytuje praktický přístup k navrhování mobilních scénářů v Dynamics 365 for Finance and Operations převzetím schválení faktur dodavatele pro mobilní zařízení jako příklad použití.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0a84027959334f96b0996299c1b0b092435972a7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837365"
---
# <a name="mobile-invoice-approvals"></a>Mobilní schvalování faktur

[!include [banner](../includes/banner.md)]

Mobilní funkce v aplikaci Microsoft Dynamics 365 for Finance and Operations umožňují obchodnímu uživateli navrhovat mobilní rozhraní. Pro pokročilé scénáře platforma také vývojářům umožňuje rozšířit možnosti podle vlastních potřeb. Nejúčinnějším způsobem, jak se naučit některé nové pojmy v oblasti mobilních zařízení, je projít proces navrhování několik scénářů. Toto téma poskytuje praktický přístup k navrhování mobilních scénářů převzetím schválení faktur dodavatele pro mobilní zařízení jako příklad použití. Toto téma by vám mělo pomoci navrhnout jiné varianty scénářů a lze je také použít pro další scénáře, které nesouvisejí s fakturami dodavatele.

<a name="prerequisites"></a>Požadavky
-------------

| Předpoklad                                                                                            | popis                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Předběžná verze mobilní příručky                                                                                |[Mobilní platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 for Finance and Operations                                                                             | Prostředí, které má Microsoft Dynamics 365 for Operations verzi 1611 a Microsoft Dynamics for Operations s aktualizací Platform Update 3 (listopad 2016)                   |
| Nainstalujte opravu hotfix KB 3204341.                                                                              | Záznamník úloh může omylem zaznamenat dva příkazy k zavření rozevíracích dialogových oken, které jsou součástí aktualizace Dynamics 365 for Operations Platform Update 3 (aktualizace z listopadu 2016) |
| Nainstalujte opravu hotfix KB 3207800.                                                                              | Tato oprava hotfix umožňuje zobrazovat přílohy v mobilním klientovi, který je zahrnutý v Dynamics 365 for Operations Platform Update 3 (aktualizace z listopadu 2016).           |
| Nainstalujte opravu hotfix KB 3208224.                                                                              | Kód aplikace pro mobilní aplikaci schvalování faktur dodavatele je zahrnut v aplikaci Microsoft Dynamics AX 7.0.1 (květen 2016).                          |
| Zařízení se systémem Android nebo iOS nebo se systémem Windows, které má nainstalovanou mobilní aplikaci Finance and Operations | Vyhledejte aplikaci v příslušném obchodě s aplikacemi.                                                                                                                     |

## <a name="introduction"></a>Úvod
Mobilní schválení faktur dodavatele vyžadují tři opravy hotfix, které jsou uvedeny v části "Předpoklady". Tyto opravy hotfix neposkytují pracovní prostor pro schválení faktury. Chcete-li zjistit, co je pracovní prostor v souvislosti s mobilními zařízeními, přečtěte si příručku pro mobilní zařízení, která je uvedena v části "Předpoklady". Musí být navržen pracovní prostor schválení faktury. 

Každá organizace ladí a definuje svůj svůj obchodní proces pro faktury dodavatele jinak. Dříve, než navrhnete mobilní prostředí pro schválení faktury dodavatele, měli byste zvážit následující aspekty obchodního procesu. Základem je využívat tyto datové body co nejvíce, aby se optimalizovalo uživatelské prostředí v zařízení.

-   Která pole z hlavičky faktury bude uživatel chtít vidět v mobilním prostředí a v jakém pořadí?
-   Která pole z řádek faktury bude uživatel chtít vidět v mobilního prostředí a v jakém pořadí?
-   Kolik má faktura řádků? Uplatněte zde pravidlo 80-20 a optimalizujte pro 80 procent.
-   Budou uživatelé chtít vidět rozúčtování (kódování faktury) v mobilním zařízení během kontrol? Pokud je odpověď na tuto otázku Ano, zvažte následující otázky:
    -   Kolik rozúčtování (rozšířená cena, DPH, poplatky, rozdělení atd.) je pro řádek faktury k dispozici? Znovu použijte pravidlo 80-20.
    -   Mají faktury také rozúčtování v hlavičce faktury? Pokud ano, budou tato rozúčtování k dispozici v zařízení?

> [!NOTE]
> Toto téma nevysvětluje, jak upravit rozúčtování, protože tato funkce není aktuálně podporována pro mobilní scénáře.

-   Budou uživatelé chtít vidět přílohy pro fakturu na zařízení?

Návrh mobilního prostředí pro schválení faktur se liší v závislosti na odpovědích na tyto otázky. Cílem je optimalizovat uživatelské prostředí pro obchodní proces na mobilních zařízeních v organizaci. Ve zbývající části tohoto tématu se podíváme na dvě varianty scénáře, které jsou založeny na různých odpovědích na předchozí dotazy. 

Platí zásada, abyste při práci s návrhářem mobilních aplikací nezapomněli publikovat změny, aby se zabránilo ztrátě aktualizací.

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
<td>Která pole z hlavičky faktury bude uživatel chtít vidět v mobilním prostředí a v jakém pořadí?</td>
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
<td>Která pole z řádek faktury bude uživatel chtít vidět v mobilního prostředí a v jakém pořadí?</td>
<td><ol>
<li>Kategorie zásobování</li>
<li>Množství</li>
<li>Jedn. cena</li>
<li>Čistá částka řádku</li>
<li>Částka sestavy 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kolik má faktura řádků? Uplatněte zde pravidlo 80-20 a optimalizujte pro 80 procent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Budou uživatelé chtít vidět rozúčtování (kódování faktury) v mobilním zařízení během kontrol?</td>
<td>Ano</td>
</tr>
<tr class="odd">
<td>Kolik rozúčtování (rozšířená cena, DPH, poplatky atd.) je pro řádek faktury k dispozici? Znovu použijte pravidlo 80-20.</td>
<td>Rozšířená cena: 2 DPH 2: 0 Poplatky: 0</td>
</tr>
<tr class="even">
<td>Mají faktury také rozúčtování v hlavičce faktury? Pokud ano, budou tato rozúčtování k dispozici v zařízení?</td>
<td>Nepoužito</td>
</tr>
<tr class="odd">
<td>Budou uživatelé chtít vidět přílohy pro fakturu na zařízení?</td>
<td>Ano</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Vytvoření pracovního prostoru

1.  V prohlížeči otevřete Finance and Operations a přihlaste se.
2.  Po přihlášení přidejte k adrese URL **&mode=mobile**, jak ukazuje následující příklad, a aktualizujte stránku: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  Klikněte na tlačítko **Nastavení** (ozubené kolo) v pravém horním rohu stránky, a pak klikněte na **Mobilní aplikace**. Návrhář mobilní aplikace se musí zobrazit stejně jako Záznam úloh.
4.  Kliknutím na tlačítko **Přidat** vytvořte nový pracovní prostor. V tomto příkladu pojmenujte pracovní prostor **Moje schválení**.
5.  Zadejte popis.
6.  Vyberte barvu pracovního prostoru. Barva pracovního prostoru bude použita pro celkový styl mobilního prostředí pro tento pracovní prostor.
7.  Vyberte ikonu pracovního prostoru.
8.  Klikněte na tlačítko **Hotovo**.
9.  Kliknutím na **Publikovat pracovní prostor** uložte změny

### <a name="vendor-invoices-assigned-to-me"></a>Faktury dodavatele přiřazené mně

První mobilní stránka, kterou byste měli navrhnout, je seznam faktur, které jsou přiřazeny uživateli na revizi. Při navrhování této mobilní stránky použijte stránku **VendMobileInvoiceAssignedToMeListPage** v aplikaci Finance and Operations. Před provedením tohoto postupu se ujistěte, že alespoň jedna dodavatelská faktura je vám přiřazena na revizi a že má řádek faktury dvě rozkontace. Toto nastavení splňuje požadavky pro tento scénář.

1.  V adrese URL aplikace Finance and Operations nahraďte název položky nabídky hodnotou **VendMobileInvoiceAssignedToMeListPage** k otevření mobilní verze stránky se seznamem **Nevyřízené faktury dodavatele přiřazené mně** v modulu **Závazky**. V závislosti na počtu faktur, které máte v systému přidělené, se na této stránce se zobrazí tyto faktury. Pokud chcete najít konkrétní fakturu, můžete použít filtr vlevo. Nevyžadujeme ale použití konkrétní faktury pro tento příklad. Vyžadujeme pouze, aby vám byly přiřazeny některé faktury, které vám umožní navrhnout mobilní stránku. Nové stránky, které jsou k dispozici, byly navrženy speciálně pro vývoj mobilních scénářů pro faktury dodavatele. Proto je nutné použít tyto stránky. Adresa URL by měla vypadat jako následující adresa URL a po jejím zadání se musí zobrazit stránka, která je ukázána na obrázku: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Stránka Nevyřízené faktury, které jsou přiřazeny mně](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Klikněte na tlačítko **Nastavení** (ozubené kolo) v pravém horním rohu stránky, a pak klikněte na **Mobilní aplikace**.
3.  Vyberte pracovní prostor a klikněte na **Úpravy**
4.  Klepněte na tlačítko **Přidat stránku** pro vytvoření první mobilní stránky.
5.  Zadejte název jako například **Moje faktury dodavatele** a popis jako například **Faktury dodavatele přiřazené mně ke kontrole**.
6.  Klepněte na tlačítko **Hotovo**.
7.  V mobilním návrháři na kartě **Pole** klepněte na tlačítko **Vybrat pole**. Sloupce na stránce seznamu musí vypadat podobně jako na následujícím obrázku. [![Sloupce na stránce Čekající faktury dodavatele přiřazené mně](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Přidejte požadované sloupce ze stránky seznamu, které musí být zobrazeny pro uživatele na mobilní stránce. Pořadí, ve kterém přidáváte, je pořadí, ve kterém se pole zobrazí koncovému uživateli. Jediný způsob, jak změnit pořadí polí, je opětovný výběr všech polí. Na základě požadavků pro tento scénář je vyžadováno následující osm polí. Nicméně někteří uživatelé mohou považovat osm polí za příliš mnoho informací v mobilním zařízení. Nejdůležitější pole proto ukážeme v zobrazení mobilního seznamu. Zbývající pole se zobrazí v zobrazení podrobností, které můžeme navrhnout později. Nyní přidáme následující pole. Klepněte na znaménko plus (**+**) v těchto sloupcích pro přidání na mobilní stránku.
    - Název dodavatele
    - Faktura celkem
    - Účet faktury
    - Číslo faktury
    - Datum fakturace

    Po přidání polí musí mobilní stránka vypadat podobně jako na následujícím obrázku. 
    [![Stránka po přidání polí](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Nyní také musíte přidat následující sloupce, abychom mohli později povolit akce pracovního postupu.
    - Zobrazit dokončené úkoly
    - Zobrazit úkol delegování
    - Zobrazit úkol odvolání
    - Zobrazit úkol odmítnutí
    - Zobrazit úkol požadavku na dokončení
    - Zobrazit úkol opětovného odeslání

10. Kliknutím na **Hotovo** ukončete režim úprav.
11. Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru
12. Kliknutím na **Publikovat pracovní prostor** uložte práci.
13. Povolte možnost **Zobrazit souhrn faktur u nevyřízených faktur dodavatele** ve formuláři Parametry závazků pod možností **Faktura**. Všimněte si, že pouze tím, že tento parametr povolíte, budou součty faktury vypočteny tak, aby se zobrazovaly na stránce seznamu faktur dodavatele čekajících na vyřízení. To je nová funkce v rámci nezbytné opravy hotfix 3208224.

### <a name="vendor-invoice-details"></a>Detaily faktury dodavatele

Pokud chcete navrhnout stránky podrobností faktury pro mobilní zařízení, použijte stránku **VendMobileInvoiceHeaderDetails** v aplikaci Finance and Operations. Všimněte si, že v závislosti na počtu faktur, které máte v systému, tato stránka zobrazuje nejstarší faktury (faktura, která byla vytvořena jako první). Pokud chcete najít konkrétní fakturu, můžete použít filtr vlevo. Nevyžadujeme ale použití konkrétní faktury pro tento příklad. Vyžadujeme pouze některá data faktury, abychom mohli navrhnout mobilní stránku. [![Stránka workflowu](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. V adrese URL Finance and Operations nahraďte název položky nabídky názvem **VendMobileInvoiceHeaderDetails** k otevření formuláře
2. Otevřete mobilní návrhář z tlačítka **Nastavení** (ozubené kolečko).
3. Kliknutím na tlačítko **Upravit** spusťte režim úprav v pracovním prostoru.
4. Vyberte stránku **Moje faktury dodavatele**, kterou jste vytvořili dříve, a klikněte na **Upravit**.
5. Na kartě **Pole** klikněte na záhlaví sloupce **Mřížka**.
6. Klikněte na **Vlastnosti&gt; Přidat stránku**. **Poznámka:** Po klepnutí na záhlaví **Mřížka** a přidání stránky je automaticky navázán vztah.
7. Zadejte název stránky, například **Detaily faktury** a popis, jako například **Zobrazení záhlaví faktury a podrobností řádku**.
8. Klikněte na **Vybrat pole**. Všimněte si, že pořadí, ve kterém přidáváte, je pořadí, ve kterém se pole zobrazí koncovému uživateli. Jediný způsob, jak změnit pořadí polí, je opětovný výběr všech polí. 
9. Na základě požadavků pro tento scénář přidejte následující pole ze záhlaví:
   - Název dodavatele
   - Faktura celkem
   - Účet faktury
   - Číslo faktury
   - Datum fakturace
   - Popis faktury
   - Datum splatnosti
   - Měna faktury

10. Z řádků mřížky na stránce přidejte následující pole:
    - Kategorie zásobování
    - Množství
    - Jedn. cena
    - Čistá částka řádku
    - Částka sestavy 1099

11. Po přidání všech polí z předchozích dvou kroků klepněte na **Hotovo**. Stránka musí vypadat podobně jako na následujícím obrázku.
    [![Stránka po přidání polí](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Kliknutím na **Hotovo** ukončete režim úprav.
13. Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru
14. Kliknutím na **Publikovat pracovní prostor** uložte práci.

### <a name="workflow-actions"></a>Akce workflowu

Chcete-li přidat akce pracovního postupu, použijte stránku **VendMobileInvoiceHeaderDetails** v aplikaci Finance and Operations. Chcete-li tuto stránku otevřít, nahraďte název položky nabídky v adrese URL, stejně jako dříve. Pak otevřete mobilní návrhář z tlačítka **Nastavení** (ozubené kolečko). Chcete-li přidat akce workflowu na stránce Podrobnosti, postupujte následovně. Musíte mít přiřazené faktury, které jsou v odpovídajícím stavu, abyste mohli provádět dostupné akce pracovního postupu.

#### <a name="record-workflow-actions"></a>Záznam akcí pracovního postupu
1.  Kliknutím na tlačítko **Upravit** spusťte režim úprav v pracovním prostoru.
2.  Vyberte stránku **Podrobnosti o faktuře** , kterou jste dříve vytvořili, a potom klepněte na tlačítko **Upravit**.
3.  Na kartě **Akce** klikněte na **Přidat akci**.
4.  Zadejte název akce, jako například **Schválit** a popis jako například **Schválit fakturu**. Všimněte si, že změní název akce, kterou zde zadáte, na název akce, která se zobrazí uživateli v mobilní aplikaci.
5.  Klepněte na tlačítko **Hotovo**.
6.  Klikněte na **Vybrat pole**.
7.  V procesu pracovního postupu, přejděte an stránku **VendMobileInvoiceHeaderDetails** a proveďte akci, kterou chcete nahrát. Zadejte komentáře pracovního postupu během tohoto procesu tak, aby pole komentáře bylo také součástí mobilního prostředí.
8.  Po spuštění akce pracovního postupu klepněte na **Hotovo** k dokončení úkolu Vybrat pole.
9.  Kliknutím na **Hotovo** ukončete režim úprav.
10. Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru
11. Kliknutím na **Publikovat pracovní prostor** uložte práci.
12. Opakujte předchozí kroky k zaznamenání všech požadovaných akcí pracovního postupu. 

#### <a name="create-a-js-file"></a>Vytvoření souboru .js
1. Otevřete Poznámkový blok nebo Microsoft Visual Studio a vložte následující kód. Uložit soubor jako soubor .js Tento kód provádí následující úkony:
    - Skryje sloupce týkající se pracovního postupu, které jsou navíc a které jsme přidali dříve na stránce Mobilní seznam. Můžeme přidat tyto sloupce tak, aby aplikace měla tyto informace v kontextu a provést další krok.
    - Podle kroku pracovního postupu, který je aktivní, použije logiku, aby se zobrazily pouze akce.

> [!NOTE]
> Všimněte si, že název stránky a další ovládací prvky v kódu musí být stejné jako názvy v pracovním prostoru.

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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

2.  Nahrajte kód souboru do pracovního prostoru výběrem karty **Logika**
3.  Kliknutím na **Hotovo** ukončete režim úprav.
4.  Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru
5.  Kliknutím na **Publikovat pracovní prostor** uložte práci.

### <a name="vendor-invoice-attachments"></a>Přílohy faktury dodavatele

1. Klikněte na tlačítko **Nastavení** (ozubené kolo) v pravém horním rohu stránky, a pak klikněte na **Mobilní aplikace**.
2. Kliknutím na tlačítko **Upravit** spusťte režim úprav v pracovním prostoru.
3. Vyberte stránku <strong>Podrobnosti o faktuře**, kterou jste dříve vytvořili, a potom klikněte na **Upravit</strong>.
4. Nastavte možnost **Správa dokumentů** na **Ano**, jak je ukázáno níže. **Poznámka:** Pokud neexistují žádné požadavky na mobilním zařízení, můžete nechat tuto možnost nastavenou na **Ne**, což je výchozí nastavení.
   ![Správa dokumentů](./media/docmanagement-216x300.png)
5. Kliknutím na **Hotovo** ukončete režim úprav.
6. Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru
7. Kliknutím na **Publikovat pracovní prostor** uložte práci.

### <a name="vendor-invoice-line-distributions"></a>Distribuce řádky faktury dodavatele

Požadavky pro tento scénář potvrzují, že budou existovat pouze distribuce na úrovni řádku a faktura bude mít vždy pouze jeden řádek. Vzhledem k tomu, že tento scénář je jednoduchý, musí být natolik jednoduché, že uživatel nemusí zobrazit podrobnosti k zobrazení distribucí několik úrovní uživatelského prostředí na mobilním zařízení. Faktury dodavatele v aplikaci Finance and Operations zahrnují možnost zobrazení všech distribucí z hlavičky faktury. Toto prostředí potřebujeme pro mobilní scénář. Proto použijeme stránku **VendMobileInvoiceAllDistributionTree** k navržení této části mobilního scénáře. 

> [!NOTE] 
> Znalost požadavků nám pomáhá určit, které konkrétní stránky používat a jak přesně optimalizovat mobilní prostředí pro uživatele, když navrhujeme scénář. Ve druhém scénáři použijeme jinou stránku k zobrazení rozúčtování, protože se liší požadavky pro tento scénář.

1.  V adrese URL nahraďte název položky nabídky jako předtím. Stránky, které se objeví, by měly vypadat jako na následujícím obrázku.
[![Stránka Všechny distribuce](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Otevřete mobilní návrhář z tlačítka **Nastavení** (ozubené kolečko).
3.  Kliknutím na tlačítko **Upravit** spusťte režim úprav v pracovním prostoru. **Poznámka:** uvidíte, že byly automaticky vytvořeny dvě nové stránky. Systém vytvoří tyto stránky, protože jste v předchozí části aktivovali správu dokumentů. Tyto nové stránky můžete ignorovat.
4.  Klikněte na **Přidat stránku**.
5.  Zadejte název stránky, například **zobrazení účetních** a popis, jako například **zobrazení účtování faktury**.
6.  Klepněte na tlačítko **Hotovo**.
7.  Na kartě **Pole** klikněte na **Vybrat pole**, ze stránek distribuce vyberte následující pole a potom klepněte na tlačítko **Hotovo**:
    1.  Částka
    2.  Měna
    3.  Účet hlavní knihy

    > [!NOTE] 
    > Nevybrali jsme slupec **Popis** z mřížky distribuce, protože požadavky pro tento scénář potvrdily, že výsledná cena je jediná částka, pro kterou bude existovat rozúčtování. Uživatel proto nebude vyžadovat další pole k určení typu částky, pro niž je distribuce určená. V dalším scénáři však **budeme** tyto informace používat, protože požadavky na tuto situaci určují, že jiné typy částek mají rozdělení (například DPH).
8.  Kliknutím na **Hotovo** ukončete režim úprav.
9.  Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru
10. Kliknutím na **Publikovat pracovní prostor** uložte práci.

> [!NOTE] 
> Mobilní stránka **Zobrazení účetnictví** není momentálně propojena s žádnou z mobilních stránek, které jsme doposud vytvořili. Protože by měl uživatel být schopen přejít na stránku **zobrazení účetnictví** stránky ze stránky **Detaily faktury** na mobilním zařízení, musíme poskytnout navigaci ze stránky **Detaily faktury** na stránku **Zobrazit účetnictví**. Můžeme navázat tuto navigaci pomocí další logiky pomocí jazyka JavaScript.

1.  Otevřete soubor .js, který jste vytvořili dříve a přidejte zvýrazněné řádky v následujícím kódu. Tento kód provádí dvě věci:
    1.  Pomáhá zajistit, že uživatelé nebudou moci přejít přímo z pracovního prostor na stránku **Zobrazení účtování**.
    2.  Naváže ovládání navigace ze stránky **Detaily faktury** na stránku **Zobrazení účetnictví**.

> [!NOTE] 
> Všimněte si, že název stránky a další ovládací prvky v kódu musí být stejné jako názvy v pracovním prostoru.

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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

2.  Nahrajte kód souboru do pracovního prostoru výběrem karty **Logika** pro přepis předchozího kódu
3.  Kliknutím na **Hotovo** ukončete režim úprav.
4.  Klikněte na **Zpět** a potom na **Hotovo** pro odchod z pracovního prostoru
5.  Kliknutím na **Publikovat pracovní prostor** uložte práci.

### <a name="validation"></a>Ověření

Z mobilního zařízení otevřete aplikace a připojte se k vaší instanci aplikace Finance and Operations. Ujistěte se, že jste přihlášení se do společnosti, kde vám byly faktury dodavatele přiřazeny k revizi. Je třeba provést následující akce:

-   Viz pracovní prostor **Moje schválení**.
-   Přejděte do pracovního prostoru **Moje schválení** a zobrazte stránku **Moje faktury dodavatele**.
-   Přejděte k podrobnostem na stránce **Moje faktury dodavatele** a zobrazte seznam faktur, které vám byly přiřazeny.
-   přejděte na podrobnosti jedné z faktu a zobrazte podrobnosti faktury záhlaví a podrobností řádků.
-   Na stránce Podrobnosti viz odkaz na přílohy a pomocí tohoto odkazu můžete přejít na seznam příloh a přílohy zobrazit.
-   na stránce podrobností zobrazte odkaz na stránku **Zobrazit účetnictví**  a pomocí tohoto odkazu můžete přejít na seznam příloh a přílohy zobrazit.
-   Na stránce Podrobnosti klepněte na nabídku **akce** a proveďte akce pracovního postupu, které jsou použitelné pro krok pracovního postupu.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Návrh scénáře schválení složité faktury pro společnosti Fabrikam
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
<td>Která pole z hlavičky faktury bude uživatel chtít vidět v mobilním prostředí a v jakém pořadí?</td>
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
<td>Která pole z řádek faktury bude uživatel chtít vidět v mobilního prostředí a v jakém pořadí?</td>
<td><ol>
<li>Kategorie zásobování</li>
<li>Množství</li>
<li>Jedn. cena</li>
<li>Čistá částka řádku</li>
<li>Částka sestavy 1099</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kolik má faktura řádků? Uplatněte zde pravidlo 80-20 a optimalizujte pro 80 procent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Budou uživatelé chtít vidět rozúčtování (kódování faktury) v mobilním zařízení během kontrol?</td>
<td>Ano</td>
</tr>
<tr class="odd">
<td>Kolik rozúčtování (rozšířená cena, DPH, poplatky atd.) je pro řádek faktury k dispozici? Znovu použijte pravidlo 80-20.</td>
<td>Rozšířená cena: 2 DPH 2: 2 Poplatky: 2</td>
</tr>
<tr class="even">
<td>Mají faktury také rozúčtování v hlavičce faktury? Pokud ano, budou tato rozúčtování k dispozici v zařízení?</td>
<td>Nepoužito</td>
</tr>
<tr class="odd">
<td>Budou uživatelé chtít vidět přílohy pro fakturu na zařízení?</td>
<td>Ano</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>Další kroky

Tyto změny lze provést pro scénář 1, na základě požadavků pro scénář 2. Informace v této části slouží k vylepšení zkušenosti mobilní aplikace.

1.  Vzhledem k tomu, že další řádky faktury jsou očekávány ve scénáři 2, následující změny návrhu vám pomohou optimalizovat uživatelské prostředí na mobilním zařízení:
    1.  Místo zobrazení řádků faktury na stránce Podrobnosti (jako v scénáři 1), mohou uživatelé zobrazit řádky na samostatné mobilní stránce.
    2.  Vzhledem k tomu, že v tomto případě se očekává více než jeden řádek faktury, pokud je použita stránka **VendMobileInvoiceAllDistributionTree** k vytvoření stránky distribucí pro mobilní telefon (jako v scénáři 1), může být matoucí pro uživatele při korelaci na rozdělování řádků. Proto k návrhu stránek distribuce použijte stránku **VendMobileInvoiceLineDistributionTree**.
    3.  V ideálním případě by rozdělení v tomto scénáři měla zobrazovat v kontextu řádku faktury. Proto se ujistěte, že uživatel může přejít k podrobnostem řádky, aby viděl stránku distribuce. Použijte možnost odkazu stránky k navázat procházení na detaily, stejně jako u stránek záhlaví a podrobností v scénáři 1.

2.  Vzhledem k tomu, že na rozdělení v scénáři 2 (prodejní daně, poplatky a tak dále) se očekává více než jeden typ částky, je užitečné zobrazit popis typu Částka. (Tyto informace jsme v scénáři 1 vynechali).




