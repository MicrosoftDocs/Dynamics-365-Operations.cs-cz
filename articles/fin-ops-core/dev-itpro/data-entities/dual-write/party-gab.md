---
title: Strana a globální adresář
description: Toto téma popisuje funkci strany a globálního adresáře duálního zápisu.
author: RamaKrishnamoorthy
ms.date: 08/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 127b4092ad3c5e8737aff43f503e0a8f36ff1ec8
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781337"
---
# <a name="party-and-global-address-book"></a>Strana a globální adresář

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

*Strana* a *globální adresář* jsou pojmy aplikací Finance and Operations. Stranou může být osoba nebo organizace. Je vhodné globálně ukládat a spravovat vlastnosti strany, například jméno, jazyk, kontakty a adresy. Poté, když se hodnota vlastnosti změní na jednom místě, projeví se to na všech místech, kde je strana zapojena.

## <a name="party"></a>Strana

Strana je osoba nebo organizace zapojená do podnikání. Použitím konceptu strany může osoba nebo organizace hrát v podniku více než jednu roli (pracovník, zákazník, dodavatel nebo kontakt). Role je založena na kontextu a účelu. Zde je několik příkladů rolí pro dvě fiktivní společnosti Contoso a Fabrikam:

+ **Pracovník** - Zaměstnanec. Příkladem je zaměstnanec společnosti Contoso.
+ **Dodavatel** - Dodavatelská organizace nebo jediný majitel, který dodává zboží či služby nějakému podniku. Například pokud Fabrikam prodává zásoby společnosti Contoso, Fabrikam je pro Contoso prodejcem.
+ **Kontakt** - Osoba, kterou je třeba kontaktovat. Například pokud společnost Contoso nakupuje zásoby od společnosti Fabrikam, zaměstnanci společnosti Contoso by se spojili s kontaktem ve společnosti Fabrikam.
+ **Zákazník** - Zákazník je osoba nebo společnost, která nakupuje věci od společnosti. Například pokud společnost Contoso nakupuje zásoby od společnosti Fabrikam, společnost Contoso je zákazníkem společnosti Fabrikam.

Model strany se často používá k reprezentaci středních až složitých vztahů mezi organizacemi a lidmi, zvláště když strana hraje více než jednu roli. Několik běžných příkladů:

+ Strana může být zákazníkem i dodavatelem. Například v Severní Americe společnost Fabrikam prodává elektrické dráty společnosti Contoso a nakupuje sestavené reproduktory od společnosti Contoso. V Evropě Fabrikam prodává díly společnosti Contoso, ale nic od společnosti Contoso nekupuje.
+ Strana může být zaměstnancem i zákazníkem. Například zaměstnanec společnosti Contoso nakupuje elektroniku od společnosti Contoso pro osobní použití.
+ Mezi člověkem a organizací může existovat vztah N:N. Například společnost Fabrikam dodává servisní specialisty a zaměstnává koordinátora umístění. Koordinátor přiděluje servisní specialisty k pracovním požadavkům od několika zákazníků společnosti Fabrikam. Contoso je jedním ze zákazníků společnosti Fabrikam. Když společnost Contoso potřebuje odborníka, kontaktuje koordinátora, který pak žádost zprostředkuje. Protože koordinátor umístění zpracovává požadavky pro všechny zákazníky, jedná se o vztah N: N.

Následující obrázek ukazuje datový model pro stranu:

![Datový model pro stranu.](media/party-gab-image1.png)

> [!TIP]
> Když se pokoušíte vytvořit nový záznam účtu, použijte pole **Strana** k vyhledání záznamu podle názvu. Tímto způsobem, pokud najdete záznam, stačí jej vybrat. Systém automaticky vyplní všechna data ze strany. Nemusíte ručně zadávat všechna požadovaná pole. Toto chování najdete na integrovaných formulářích na stránkých **Účet**, **Kontakt** a **Dodavatel**.

Duální zápis nepodporuje všechny role stran aplikací Finance and Operations. Úplný seznam rolí stran najdete v části [Přehled globálního adresáře](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Globální adresář

Globální adresář je adresář poštovních a elektronických adres organizací a jednotlivců účastnících se podnikání.

Globální adresář ukládá a zpracovává tolik poštovních adres a elektronických adres, kolik je potřeba. Kupříkladu má společnost Fabrikam čerpací stanice na 50 místech. Každé místo má jinou poštovní adresu, e-mailovou odresu a telefonní číslo. Všechny nákupy jsou účtovány na hlavní čerpací stanici, ale dodávány přímo na konkrétní čerpací stanici, která o nákup požádala. Globální adresář ukládá hlavní čerpací stanici jako fakturační adresu a každou čerpací stanici jako dodací adresu společnosti Fabrikam. Adresy lze uložit jednou a podle potřeby je načítat pro nabídky a objednávky.

V závislosti na obchodním kontextu může osoba nebo organizace hrát více než jednu roli a pro všechny role může být použita stejná poštovní adresa a elektronická adresa. V takovém případě by se změna adresy v jedné roli měla objevit v jiných rolích. Globální adresář ukládá a zpracovává adresy globálně.

Následující ilustrace znázorňuje datový model pro globální adresář.

![Datový model pro globální adresář.](media/party-gab-image2.png)

## <a name="contact"></a>Kontakt

V aplikacích pro zapojení zákazníků je kontakt osobou. Nicméně tabulka **Kontakt** byla přetížena, aby představovala osobu, uživatele portálu, koncového zákazníka (B2C) nebo dodavatele. Reprezentace je implicitní a bez prozkoumání souvisejících transakcí nerozeznáte rozdíl. Tabulka **Kontakt** byla omezena na relaci 1:1 s tabulkou **Účet**. Jako součást modelu strany a globálního adresáře přináší duální zápis explicitní vlastnosti pro klasifikaci, a duální zápis umožňuje vztahy N:N mezi osobou kontakt a organizací (entitou **Účet** nebo entitou **Dodavatel**).

Existují dva typy řádků **Kontakt**:

+ **Prokládaný kontakt** – řádek **Kontakt** s povinnou hodnotou v poli **Společnost**.
+ **Neprokládaný kontakt** – řádek **Kontaktu** s prázdným polem **Společnost**.

Tabulka **Kontakt** může ukládat tyto typy řádků:

| Typ řádku | popis |
|----------|-------------|
| Osoba, která je zákazníkem (například prodejní kontakt nebo zákazník B2C) | Záznam prokládaného kontaktu, kde pole **Společnost** není prázdné a pole **Je zákazník** je nastaveno na **Ano**. |
| Osoba, která je dodavatelem (například jediný vlastník, jako je dodavatel) | Záznam prokládaného kontaktu, kde pole **Společnost** není prázdné a pole **Je dodavatel** je nastaveno na **Ano**. |
| Osoba,, která je zákazníkem i dodavatelem | Záznam prokládaného kontaktu, kde pole **Společnost** není prázdné, pole **Je zákazník** je nastaveno na **Ano** a pole **Je dodavatel** je nastaveno na **Ano**. Osoba může být jak výrobcem jednoho produktu, tak spotřebitelem jiného produktu. Tuto relaci podporují jak aplikace Finance and Operations, tak duální zápis. |
| Osoba, která je kontaktní osobou pro organizaci, ale není zákazníkem ani prodejcem. | Záznam neprokládaného kontaktu, kde pole **Společnost** je prázdné, pole **Je zákazník** je nastaveno na **Ne** a pole **Je dodavatel** je nastaveno na **Ne**. |

## <a name="contact-for-party-table"></a>Tabulka kontaktu pro stranu

Tabulka **Kontakt pro stranu** ukládá a zpracovává vztahy N: N mezi řádky tabulky **Účet** a řádky tabulky **Kontakt**. Prokládané řádky tabulky **Kontakt** můžete odfiltrovat od neprokládaných řádků a přidružit pouze neprokládané řádky **Kontakt** k řádkům tabulek **Účet** nebo **Dodavatel**.

Například Natasha Jones a Miguel Reyes jsou veterináři, kteří se starají o farmy ve svých oblastech. Natasha obsluhuje oblast Seattle a Miguel obsluhuje oblast Kent. V aplikaci pro interakci se zákazníky jsou farmy vyjádřeny jako zákazníci a veterináři jsouv roli kontaktní osoby. Jediný záznam **Kontakt** pro Natašu je spojen se všemi farmami, na kterých Nataša pracuje. Obdobně je jediný záznam **Kontakt** pro Miguela spojen se všemi farmami, na kterých Miguel pracuje.

Tyto relace jsou uloženy v tabulce **Kontakt pro stranu**. Tyto informace najdete na integrovaných formulářích na stránkých **Účet**, **Kontakt** a **Dodavatel**.

+ Na stránce **Účet** můžete použít záložku **Přidružené kontakty** pro přidružení jednoho nebo více kontaktů k řádku **Účet**. Takto přiřazujete kontaktní osobu pro organizaci. Poté můžete vybrat jeden kontakt jako primární kontakt pro účet. Pokud používáte stránku **Rychlé vytvoření**, můžete vybrat pouze kontaktní osobu. Chování je stejné, když používáte stránku **Dodavatel** a typ záznamu je **Organizace**.
+ Na stránce **Kontakt**, pokud je řádkem zákazník, prodejce nebo obojí (prokládaný kontakt), můžete použít kartu **Přidružené kontakty** k přidružení jednoho nebo více kontaktů. Takto přiřazujete kontaktní osobu pro zákazníka nebo dodavatele B2C. Poté můžete vybrat jeden kontakt jako primární kontakt. Pokud používáte stránku **Rychlé vytvoření**, můžete vybrat pouze kontaktní osobu.
+ Na stránce **Kontakt**, pokud je řádkem kontaktní osoba (neprokládaný kontakt), můžete použít kartu **Přidružené organizace** k přidružení jednoho nebo více kontaktů. Takto přiřazujete zákazníky nebo dodavatele k základní kontaktní osobě. Zákazníkem nebo prodejcem může být organizace, osoba nebo obojí. Ze čtyř polí můžete vybrat pouze jednu hodnotu současně:

    + Když zvolíte hodnotu v poli **ID strany**, poté je základní kontakt přiřazen všem rolím vybrané strany.
    + Když zvolíte hodnotu v poli **Přidružený kontakt**, pak vybíráte prokládaný kontakt typu **Osoba**.
    + Pokud vyberete hodnotu v poli **Přidružený účet** nebo **Přidružený prodejce**, vybíráte organizaci.

    ![Karta Přidružené organizace na stránce Kontakt.](media/party-gab-image3.png)

    Bez ohledu na váš výběr je přidružení vytvořeno na úrovni strany a je použitelné na všechny role strany a je uloženo v entitě **Kontakt pro stranu**.

> [!NOTE]
> Zobrazovaný název pro tabulku **Kontakt pro stranu** v aplikacích pro zapojení zákazníků je **Kontakt pro zákazníka/dodavatele**.

Když otevřete řádek **Kontakt**, ve kterém jsou jak pole **Je zákazník** tak **Je prodejce** nastaveny na **Ne**, zobrazí se karta **Přidružené organizace**. Tato karta slouží k přidružení jedné nebo více organizací zákazníka nebo dodavatele ke kontaktu.

Když otevřete řádek **Kontakt**, ve kterém jsou pole **Je zákazník** nebo **Je prodejce** nastaveny na **Ano**, zobrazí se karta **Přidružené kontakty**. Tato karta slouží k přidružení jednoho nebo více kontaktů.

## <a name="postal-addresses"></a>Poštovní adresy

Do formulářů **Účet**, **Kontakt** a **Dodavatel** byla přidána nová stránka s názvem **Adresy**. Tato karta podporuje více poštovních adres pomocí mřížky, jak je znázorněno na následujícím obrázku.

![Mřížka pro poštovní adresy.](media/party-gab-image4.png)

Mřížka obsahuje následující sloupce:

+ **Role poštovní adresy** - Uvádí účel poštovní adresy.
+ **Je primární** - Hodnota, která označuje, zda je adresa primární adresou.
+ **Číslo adresy** - Pořadí adres.

Můžete použít tlačítko **Nová adresa** nad mřížkou k vytvoření tolika poštovních adres, kolik chcete.

Pole **Adresa 1** a **Adresa 2** na kartě **Souhrn** stránky **Účet** odpovídají adresám **Dodávka** a **Faktura**.

![Karta Souhrn pro poštovní adresy.](media/party-gab-image5.png)

Pole **Adresa 1**, **Adresa 2** a **Adresa 3** na kartě **Souhrn** stránky **Kontakt** odpovídají adresám **Podnik**, **Dodávka** a **Faktura**.

## <a name="electronic-addresses"></a>Elektronické adresy

Do formulářů **Elektronické adresy**, **Kontakt** a **Dodavatel** byla přidána nová stránka s názvem **Adresy**. Tato karta podporuje více elektronických adres pomocí mřížky, jak je znázorněno na následujícím obrázku.

![Mřížka pro elektronické adresy.](media/party-gab-image6.png)

Mřížka obsahuje následující sloupce:

+ **Typ** - Typ elektronické adresy.
+ **Je primární** Hodnota, která označuje, zda je adresa primární adresou.
+ **Účel** - Účel elektronické adresy.

Můžete použít tlačítko **Nová elektronická adresa** nad mřížkou k vytvoření tolika elektronických adres, kolik chcete.

Elektronické adresy jsou k dispozici pouze v této mřížce. V budoucích verzích budou všechna pole elektronické a poštovní adresy odstraněna z jiných karet, například karet **Souhrn** a **Detaily**. Kontaktní údaje zobrazené na kartě **Podrobnosti** jsou kopie primární elektronické adresy pouze pro čtení, jako je primární telefon, primární e-mail, primární fax a primární Twitter ID. Během procesu kvalifikace zájemce můžete zadat obchodní telefonní číslo i číslo mobilního telefonu. Firemní telefonní číslo je považováno za primární telefon, pokud **IsMobile=No** a číslo mobilního telefonu je považováno za sekundární telefon, pokud **IsMobile=Yes**.

> [!TIP]
> Použití karet **Adresy** a **Elektronické adresy** ve formulářích **Obchodní vztah** a **Kontakt** pro správu poštovních a elektronických adres. Tím je zajištěno, že se data adres synchronizují s aplikací Finance and Operations.

## <a name="setup"></a>Nastavení

1. Otevřete prostředí aplikace pro zapojení zákazníků.

2. Nainstalujte si nejnovější verzi (2.2.2.60 nebo novější) z [Řešení orchestrace aplikace s duálním zápisem](https://aka.ms/dual-write-app).

3. Nainstalujte [Řešení strany a globálního adresáře s duálním zápisem](https://aka.ms/dual-write-gab).

4. Otevřete aplikaci Finance and Operations. Přejděte do modulu Správa dat a vyberte kartu Duální zápis. Otevře se stránka pro správu duálního zápisu.

5. Aplikujte obě řešení nainstalovaná v krocích 2 a 3 pomocí funkce [Použít řešení](link-your-environment.md).

6. Ukončete následující mapování, protože již nejsou nutná. Místo toho spusťte mapu `Contacts V2 (msdyn_contactforparties)`.

    + Kontakty CDS V2 a Kontakty (týká se zákaznických kontaktů)
    + Kontakty CDS V2 a Kontakty (týká se dodavatelských kontaktů)

7. Následující mapování entit jsou aktualizována pro funkčnost strany, takže na tato mapování musí být použita nejnovější verze.

    Zobrazit na mapě | Aktualizujte na tuto verzi | Změny
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.5 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Customers V3 (accounts)` | 1.0.0.5 |Odebráno `PartyNumber` a další pole týkající se strany, jako je jméno, osobní detaily, pole poštovní adresy, pole elektronické kontaktní adresy atd.
    `Customer V3 (contacts)` | 1.0.0.5 | Odebráno `PartyNumber` a další pole týkající se strany, jako je jméno, osobní detaily, pole poštovní adresy, pole elektronické kontaktní adresy atd.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Odebráno `PartyNumber` a další pole týkající se strany, jako je jméno, osobní detaily, pole poštovní adresy, pole elektronické kontaktní adresy atd.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Nahrazuje kontaktní osobu referencí `ContactforParty`.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Nahrazuje kontaktní osobu referencí `ContactforParty`.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Nahrazuje kontaktní osobu referencí `ContactforParty`.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Toto je nová mapa přidaná jako součást tohoto vydání.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.1 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Complimentary Closings ( msdyn_compliemntaryclosings)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Toto je nová mapa přidaná jako součást tohoto vydání.

8. Před spuštěním výše uvedených map musíte ručně aktualizovat integrační klíče, jak je popsáno v následujících krocích. Pak vyberte **Uložit**.

    | Zobrazit na mapě | Klíče |
    |-----|------|
    | Účet |  accountnumber [Číslo účtu]<br>msdyn_company.cdm_companycode [společnost (Kód společnosti)] |
    | Kontakt | msdyn_contactpersonid [Číslo účtu / ID kontaktní osoby]<br>msdyn_company.cdm_companycode [společnost (Kód společnosti)] |
    | Kontakt na zákazníka/Prodejce | msdyn_contactforpartynumber [Kontakt na číslo strany]<br>msdyn_associatedcompanyid.cdm_companycode [Přidružená společnost (Kód společnosti)] |
    | Dodavatel | msdyn_vendoraccountnumber [Číslo účtu dodavatele]<br>msdyn_company.cdm_companycode [společnost (Kód společnosti)]|

9. v Dataverse, limity počtu znaků pravidel pro detekci duplikátů se zvýšily ze 450 na 700 znaků. Tento limit umožňuje přidat jeden nebo více klíčů k pravidlům detekce duplikátů. Rozbalte pravidlo pro detekci duplikátů pro tabulku **Účty** nastavením následujících polí.

    | Pole | Hodnota |
    |-------|-------|
    | Jméno | Účty se stejným názvem účtu. |
    | popis | Zjistí záznamy účtu, které mají stejnou hodnotu v atributu Název účtu. |
    | Základní typ záznamu | Účet |
    | Odpovídající typ záznamu | Účet |
    | Název účtu (pole) | Přesná shoda |
    | Společnost (pole) | Přesná shoda |
    | Typ vztahu (pole) | Přesná shoda |
    | ID strany (pole) | Přesná shoda |
    | Výběr (pole) | (prázdné) |

    ![Duplicitní pravidlo pro účty.](media/duplicate-rule-1.PNG)

10. Rozbalte pravidlo pro detekci duplikátů pro tabulku **Kontakty** nastavením následujících polí.

    | Pole | Hodnota |
    |-------|-------|
    | Jméno | Kontakty se stejným křestním jménem a příjmením. |
    | popis | Zjistí záznamy kontaktů, které mají stejné hodnoty v polích Jméno a Příjmení. |
    | Základní typ záznamu | Kontakt |
    | Odpovídající typ záznamu | Kontakt |
    | Jméno (pole) | Přesná shoda |
    | Příjmení (pole) | Přesná shoda |
    | Společnost (pole) | Přesná shoda |
    | ID strany (pole) | Přesná shoda |
    | Výběr (pole) | (prázdné) |

    ![Duplicitní pravidlo pro kontakty.](media/duplicate-rule-2.PNG)

11. Pokud jste stávajícím uživatelem a používáte dvojí zapisování, postupujte podle pokynů v [Upgrade na model strany a globálního adresáře](upgrade-party-gab.md) a upgradujte svá data.

12. Spusťte mapy v následujícím pořadí. Pokud se zobrazí chyba se stavem „Ověření projektu se nezdařilo. Chybí cílové pole ... “, otevřete mapu a vyberte **Obnovit tabulky**. Poté spusťte mapu.

    Aplikace Finance and Operations | Aplikace Customer Engagement  
    ----------------------------|------------------------
    [Strany CDS](mapping-reference.md#220) | msdyn_parties
    [Místa poštovní adresy CDS](mapping-reference.md#234) | msdyn_postaladdresscollections
    [Historie poštovní adresy CDS V2](mapping-reference.md#235) | msdyn_postaladdresses
    [Místa poštovní adresy strany CDS](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Kontakty strany V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Zákazníci V3](mapping-reference.md#101) | účty
    [Zákazníci V3](mapping-reference.md#116) | kontakty
    [Dodavatelé V2](mapping-reference.md#202) | msdyn_vendors
    [Tituly kontaktní osoby](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Zdvořilostní zakončení](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Oslovení](mapping-reference.md#228) | msdyn_salutations
    [Role v rozhodovacím procesu](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Pracovní funkce zaměstnání](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Úrovně věrnosti](mapping-reference.md#226) | msdyn_loyaltylevels
    [Typy osobní charakteristiky](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Kontakty V2](mapping-reference.md#221) | msdyn_contactforparties
    [Záhlaví prodejní nabídky CDS](mapping-reference.md#215) | nabídky
    [Záhlaví prodejní objednávky CDS](mapping-reference.md#217) | salesorders
    [Záhlaví prodejní faktury V2](mapping-reference.md#118) | faktury

> [!NOTE]
> Mapa `CDS Contacts V2 (contacts)` je mapa, kterou jste zastavili v kroku 1. Když se pokusíte spustit další mapy, mohou se tyto 2 mapy objevit v seznamu závislých osob. Nespouštějte tyto mapy.
>
> Pokud je nainstalováno řešení strany a globálního adresáře, musíte deaktivovat pojmenované připojení `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead`. Pokud odinstalujete řešení strany a globálního adresáře, musíte znovu aktivovat plugin .
>
> Pole `msdyn_*partynumber` (jednořádkové textové pole), zahrnuté v tabulkách **Účet**, **Kontakt** a **Prodejce** by se neměly v budoucnosti používat. Název štítku má předponu **(Zastaralé)** pro přehlednost. Místo toho použijte pole **msdyn_partyid**. Pole je vyhledáváním pro tabulku **msdyn_party**.

> Název tabulky | Staré pole | Nové pole
> --------|-------|--------
> Účet | `msdyn_partynumber` | `msdyn_partyid`
> Kontakt | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Šablony

Kolekce mapování tabulek pracují společně pro interakci strany a globálního adresáře, jak je uvedeno v následující tabulce.

| Aplikace Finance and Operations | Aplikace Customer Engagement | popis |
|----------------------------|-------------------------|-------------|
| [Tituly kontaktní osoby](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Zákazníci V3](mapping-reference.md#101) | účty |
| [Zákazníci V3](mapping-reference.md#116) | kontakty |
| [Strany CDS](mapping-reference.md#220) | msdyn\_parties |
| [Místa poštovní adresy strany CDS](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [Historie poštovní adresy CDS V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [Místa poštovní adresy CDS](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [Záhlaví prodejní nabídky CDS](mapping-reference.md#215) | nabídky |
| [Záhlaví prodejní objednávky CDS](mapping-reference.md#217) | salesorders |
| [Zdvořilostní zakončení](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Kontakty V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Role v rozhodovacím procesu](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Pracovní funkce zaměstnání](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Úrovně věrnosti](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Kontakty strany V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Typy osobní charakteristiky](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Záhlaví prodejní faktury V2](mapping-reference.md#118) | faktury |
| [Oslovení](mapping-reference.md#228) | msdyn\_salutations |
| [Dodavatelé V2](mapping-reference.md#202) | msdyn\_vendors |

Další informace viz [Odkaz na mapování duálního zápisu ](mapping-reference.md).

## <a name="known-issues-and-limitations"></a>Známé problémy a omezení

+ v aplikacích Finance and Operations, když vytvoříte zákazníka spolu s adresou a uložíte jej, nemusí se adresa synchronizovat s tabulkou **Adresa**. Důvodem je problém se sekvenováním platformy pro dvojí zápis. Jako řešení nejprve vytvořte zákazníka a uložte ho. Poté přidejte adresu.
+ V aplikacích Finance and Operations, když má záznam zákazníka primární adresu a vytvoříte nový kontakt pro tohoto zákazníka, pak záznam kontaktu zdědí primární adresu z přidruženého záznamu zákazníka. K tomu dochází také u kontaktu prodejce. Dataverse aktuálně toto chování nepodporuje. Pokud je povolen duální zápis, kontakt na zákazníka zdědí primární adresu z aplikace Finance and Operations je synchronizována do Dataverse spolu s jeho adresou.
+ Elektronické adresy nastavené v záložce elektronických adres tabulek **Účet**, **Kontakt** a **Dodavatel** pochází z tabulky `msdyn_partyelectronicaddress`. Tyto informace neplynou k souvisejícím transakcím, jako je prodejní objednávka, nabídka a nákupní objednávka. Plánujeme tento problém vyřešit v přírůstkové verzi. Existující data v polích elektronické adresy v záznamech účtu a kontaktů budou i nadále fungovat na transakcích, jako je prodejní objednávka, nabídka a nákupní objednávka.
+ V aplikacích Finance and Operations můžete vytvořit záznam kontaktu z formuláře **Přidat kontakt**. Když se pokusíte vytvořit nový kontakt z formuláře **Zobrazit kontakt**, akce selže. Toto je známý problém.

    ![Známý problém s Přidat kontakt.](media/party-gab-contact-issue.png)

+ **Počáteční synchronizace** nepodporuje časová pole **Dostupný z** a **K dispozici pro** v **ContactForParty**, protože DIXF převádí hodnotu na řetězec místo na celé číslo. Konverze spustí chybu `Cannot convert the literal '<say 08:00:00>’ to the expected type edm.int32`.
+ Pokud se poštovní adresa používá z více než jednoho důvodu, například adresa obchodní komunikace a fakturační adresa, měla by vypadat jako `Business;Invoice` jak je znázorněno na následujícím obrázku. Pokud mezi hodnoty přidáte mezeru, zobrazí se chyba.

    ![Známý problém s adresou.](media/party-gab-address-issue.png)

+ Poštovní adresu se zpětným datem nelze zadat pomocí aplikace Finance and Operations s duálním zápisem, protože Dataverse nepodporuje datum platnosti. Pokud zadáte poštovní adresu s datem do budoucna pomocí aplikace Finance and Operations, synchronizuje se do Dataverse úplně a uvidíte adresu na uživatelském rozhraní okamžitě. Jakékoli aktualizace tohoto záznamu budou mít za následek chybu, protože je datován do budoucnosti a není aktuální v aplikaci Finance and Operations.
