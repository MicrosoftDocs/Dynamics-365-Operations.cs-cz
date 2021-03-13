---
title: Integrace nákupu mezi Supply Chain Management a Field Service
description: Toto téma popisuje, jak integrace duálního zápisu podporuje vytváření a aktualizace nákupních objednávek jak ze Supply Chain Management, tak z Field Service.
author: RichardLuan
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c2b0d5be38425b5ceebb38b7964f5ec600b1c838
ms.sourcegitcommit: ca05440ee503bf15fe98fe138d317c1cdf21ad16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141897"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Integrace nákupu mezi Supply Chain Management a Field Service

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management poskytuje robustní funkce nákupu. Dynamics 365 Field Service nabízí podobné funkce, které podporují nákupní procesy spojené s procesem služby. Funkce v těchto dvou aplikacích jsou integrovány prostřednictvím duálního zápisu a výsledné případy použití napříč funkcemi jsou povoleny prostřednictvím mapování tabulek, logiky řešení, zobrazení a formulářů.

Tato integrace podporuje vytváření objednávek a ve většině případů aktualizace z obou aplikací. Supply Chain Management však řídí ceny, adresy a příjem produktu. Pro organizace, které používají jak Field Service, tak Supply Chain Management, je povoleno několik výkonných případů použití napříč funkcemi. Tyto případy použití umožňují zahájení a sledování nákupů v obou systémech.

Následující obrázek ukazuje tabulky v obou systémech a jejich vzájemné mapování. Nákupní objednávky ve Field Service odkazují na řádek *účet*, zatímco nákupní objednávky v Supply Chain Management odkazují na řádek *dodavatel*. K vyřešení integrace používá dvojí zápis odkaz na řádky *dodavatel* s řádky *účet*. Další informace naleznete v tématu [Integrovaný kmenový soubor dodavatele](vendor-mapping.md).

![Mapování pro zásobování](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Předpoklady

Chcete-li integrovat Supply Chain Management s Field Service, musíte nainstalovat následující součásti:

- Verze Field Service 8.8.31.60 nebo novější, pro komplexní integraci objednávek
- Supply Chain Management verze 10.0.14 nebo novější
- Duální zápis, pro spuštění řešení OneFSSCM

## <a name="installation-guidelines"></a>Pokyny k instalaci

### <a name="prerequisites"></a>Předpoklady

+ **Duální zápis** - Další informace získáte na [domovské stránce pro duální zápis](dual-write-home-page.md#dual-write-setup).
+ **Dynamics 365 Field Service** – Další informace viz [Postup instalace Dynamics 365 Field Service](https://docs.microsoft.com/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Když jsou povoleny v Microsoft Dataverse, představují duální zápis a Field Service několik vrstev řešení, která rozšiřují prostředí o nová metadata, formuláře, pohledy a logiku. Tato řešení lze povolit v libovolném pořadí, ačkoli se obvykle instalují v pořadí uvedeném zde:

1. **Field Service Common** - Field Service Common se instaluje, když je v prostředí nainstalována Field Service.
2. **Field Service (Anchor)** - Field Service (Anchor) se instaluje, když je v prostředí nainstalována Field Service. 
3. **Rozšířený Supply Chain Management** – Rozšířený Supply Chain Management se automaticky nainstaluje, když je v prostředí povolen duální zápis. 
4. **Řešení OneFSSCM** - OneFSSCM se automaticky instaluje podle toho, které řešení (Field Service nebo Supply Chain Management) je nainstalováno jako poslední.

    + Pokud je Field Service v prostředí již nainstalovaná a povolíte duální zápis, který nainstaluje rozšířený Supply Chain Management, je nainstalován OneFSSCM.
    + Pokud je rozšířený Supply Chain Management v prostředí již nainstalován a povolíte duální zápis, který nainstaluje Supply Chain Management, je nainstalován OneFSSCM.

## <a name="initial-synchronization"></a>Počáteční synchronizace

Chcete-li vytvořit nové objednávky a pracovat s existujícími objednávkami, musíte synchronizovat referenční data mezi Supply Chain Management a Dataverse. Funkci počátečního zápisu použijete k detekci vztahů tabulek a vyhledání tabulek, které musíte pro danou mapu povolit.

Musíte synchronizovat následující tabulky:

- Šablony produktu

    Při spuštění počátečního zápisu získáte úplný seznam požadovaných tabulek. Zde je několik příkladů těchto šablon:

    - Všechny výrobky
    - Uvolněné produkty V2
    - Uvolněné jedinečné produkty v Dataverse

- Pracoviště
- Sklady
- Šablony kategorií nákupu

    Zde je několik příkladů těchto šablon:

    - Kategorie zásobování
    - Pro
    - Hierarchie kategorií produktu
    - Přiřazení kategorií produktů

- Šablony dodavatele, například Vendor V2
- Šablony kontaktních osob, například Dataverse Kontakty V2
- Šablony pracovníka, například Worker

Synchronizace tabulek zajišťuje, že všechny dokumenty (nákupní objednávky a příjmy z produktů) v Supply Chain Management jsou k dispozici v Dataverse.

### <a name="account-and-vendor-tables"></a>Tabulky Účet a Dodavatel

Nákupní objednávky ve Field Service se při sledování prodejců spoléhají na tabulku účtů. Proto tabulky Dataverse pro nákupní objednávky používají ke sledování dodavatelů účty. Aby se tento klíčový rozdíl vyrovnal, je nutné aktivovat následující čtyři pracovní postupy, aby byly účty a dodavatelé synchronizovány: 

- Vytvoření dodavatelů v tabulce Účty
- Vytvoření dodavatelů v tabulce Dodavatelé
- Aktualizace dodavatelů v tabulce Účty
- Aktualizace dodavatelů v tabulce Dodavatelé

Pokud je nainstalován OneFSSCM, protože jsou nainstalovány jak Field Service, tak Supply Chain Management Extended, jsou tyto pracovní postupy automaticky aktivovány. Pokud není Field Service nainstalována, ale chcete integrovat tabulky nákupní objednávky s Dataverse, musíte tyto pracovní postupy aktivovat. V obou případech, pokud nezačnete úplně od začátku, možná budete muset zajistit, aby všichni dodavatelé byli vytvořeni jako účty v Dataverse, než vytvoříte nákupní objednávky. Jinak může dojít k chybám.

### <a name="initial-synchronization"></a>Počáteční synchronizace

Po splnění všech předpokladů, pokud chcete, aby byly v obou systémech k dispozici existující objednávky a potvrzení o produktu, musíte provést počáteční synchronizaci následujících šablon:

- Záhlaví nákupní objednávky V2
- Řádek nákupní objednávky CDS
- Měkké mazání řádku nákupní objednávky CDS
- Příjem nákupní objednávky
- Nákupní objednávka – příjemka produktu

## <a name="mappings-with-logic"></a>Mapování s logikou

Integrace nákupu rozšiřuje mapování produktu o následující logiku, aby bylo zajištěno, že sloupec **Typ produktu Field Service** je správně nastaven v tabulce produktů v Dataverse:

- Pokud je **Typ produktu** nastaven na *Produkt* a **Skupina modelů zboží, Skladový produkt** je nastaven na *Pravda*, **Typ produktu Field Service** je nastaven na *Sklad*.
- Pokud je **Typ produktu** nastaven na *Produkt* a **Skupina modelů zboží, Skladový produkt** je nastaven na *False*, **Typ produktu Field Service** je nastaven na *Jiný typ než sklad*.
- Pokud je **Typ produktu** nastaven na *Služba*, **Typ produktu Field Service** je nastaven na *Služba*.

Navíc Dataverse zahrnuje logiku, která mapuje dodavatele s jejich souvisejícími účty. Tato logika nastavuje výchozí účet dodavatele faktury. Při vytváření logika modulu plug-in na straně serveru nastaví výchozí účet dodavatele faktury od dodavatele, který souvisí s účtem. Prodejce má odkaz na fakturační účet, který se používá k nastavení této hodnoty.

## <a name="supported-scenarios"></a>Podporované scénáře

+ Nákupní objednávky lze vytvářet a aktualizovat pomocí uživatelů Dataverse. Proces a data jsou však řízeny v Supply Chain Management. Omezení týkající se aktualizací sloupců nákupních objednávek ve Supply Chain Management platí, když aktualizace pocházejí z Field Service. Nemůžete například aktualizovat nákupní objednávku, pokud byla dokončena. 
+ Pokud je nákupní objednávka řízena správou změn ve správě Supply Chain Management, může uživatel Field Service aktualizovat nákupní objednávku pouze v případě, že je stav schválení Supply Chain Management *Koncept*.
+ Několik sloupců je spravováno pouze pomocí Supply Chain Management a nelze je aktualizovat ve službě Field Service. Chcete-li zjistit, které sloupce nelze aktualizovat, zkontrolujte tabulky mapování v produktu. Z důvodu jednoduchosti je většina těchto sloupců nastavena pouze na čtení stránek Dataverse. 

    Například sloupce s informacemi o ceně jsou spravovány pomocí Supply Chain Management. Supply Chain Management má obchodní dohody, ze kterých může Field Service těžit. Sloupce jako **Jednotková cena**, **Sleva**, a **Čistá částka** pocházejí pouze ze Supply Chain Management. Abyste zajistili synchronizaci ceny se službou Field Service, měli byste použít funkci **Sync** na stránkách **Nákupní objednávka** a **Produkt na objednávku** v Dataverse při zadání údajů o objednávce. Další informace získáte v části [Synchronizace s údaji o nákupu Dynamics 365 Supply Chain Management na vyžádání](#sync-procurement).

+ Sloupec **Součty** je dostupný pouze ve službě Field Service, protože v Supply Chain Management neexistují žádné aktuální součty nákupní objednávky. Součty v Supply Chain Management se počítají na základě více parametrů, které nejsou k dispozici ve Field Service.
+ Řádky nákupní objednávky, kde je zadána pouze kategorie nákupu nebo kde je zadaný produkt položka typu produktu *Služba* nebo typ produktu Field Service, lze zahájit pouze v Supply Chain Management. Řádky se poté synchronizují do Dataverse a jsou viditelné ve Field Service.
+ Pokud je nainstalován pouze produkt Field Service a ne Supply Chain Management, sloupec **Sklad** je na objednávce povinný. Pokud je však nainstalován Supply Chain Management, je tento požadavek uvolněný, protože Supply Chain Management umožňuje řádky nákupní objednávky, kde není v určitých situacích uveden žádný sklad.
+ Příjmy z produktu (příjmy z nákupní objednávky v Dataverse) jsou spravovány pomocí Supply Chain Management a nelze z nich vytvořit Dataverse, pokud je nainstalován Supply Chain Management. Příjmy produktu ze Supply Chain Management jsou synchronizovány ze Supply Chain Management do Dataverse.
+ V Supply Chain Management je povoleno nedostatečné doručení. Řešení OneFSSCM přidává logiku, takže když je na řádku pro příjem produktu (nebo produkt příjmu nákupní objednávky v Dataverse) vytvořen nebo aktualizován, je vytvořen řádek deníku zásob Dataverse pro úpravu zbývajícího množství, které je v pořadí pro scénáře nedostatečné dodávky.

## <a name="unsupported-scenarios"></a>Nepodporované scénáře

+ Field Service zabraňuje přidání řádků do zrušené nákupní objednávky v Supply Chain Management. Jako řešení můžete změnit stav systému nákupní objednávky ve Field Service a poté přidat nový řádek do Field Service nebo Supply Chain Management.
+ Přestože řádky nákupu ovlivňují úrovně zásob v obou systémech, tato integrace nezajišťuje vyrovnání zásob napříč Supply Chain Management a Field Service. Field Service i Supply Chain Management mají další procesy, které aktualizují úrovně zásob. Tyto procesy jsou mimo rozsah nákupu.

## <a name="status-management"></a>Správa stavu

Stavy nákupních objednávek ve Field Service se liší od stavů v Supply Chain Management.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Stavy produktu Field Service a nákupní objednávky

| Záhlaví - stav systému | Záhlaví - Stav schválení | Stav položky |
|---|---|---|
| <ul><li>Koncept</li><li>Odesláno</li><li>Zrušeno</li><li>Produkt přijat</li><li>Fakturováno</li></ul> | <ul><li>Null</li><li>Schváleno</li><li>Zamítnuto</li></ul> | <ul><li>Čeká na zpracování</li><li>Přijato</li><li>Zrušeno</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Stavy Supply Chain Management a řádků nákupních objednávek pro správu

Stavy schválení řádku jsou aktivní pouze v případě, že existuje pracovní postup řádku.

| Záhlaví - stav dokumentu | Záhlaví - Stav schválení | Stav řádku | Stav schválení řádku |
|---|---|---|---|
| <ul><li>Otevření objednávky (zpětná objednávka)</li><li>Přijato</li><li>Fakturováno</li><li>Zrušeno</li></ul> | <ul><li>Koncept</li><li>Probíhá kontrola</li><li>Schváleno</li><li>Zamítnuto</li><li>Na externí kontrolu</li><li>Potvrzeno</li><li>Finalizováno</li></ul> | <ul><li>Otevření objednávky (zpětná objednávka)</li><li>Přijato</li><li>Fakturováno</li><li>Zrušeno</li></ul> | <ul><li>Neodesláno</li><li>Probíhá kontrola</li><li>Schváleno</li><li>Zamítnuto</li></ul> |

Na stavové sloupce se vztahují následující pravidla:

+ Stav v Supply Chain Management nelze z Field Service aktualizovat. V některých případech se však stav ve Field Service aktualizuje, když se změní stav nákupní objednávky v Supply Chain Management.
+ Pokud je nákupní objednávka v Supply Chain Management ve správě změn a zpracovává se změna, je stav schválení *Koncept* nebo *Probíhá kontrola*. V tomto případě bude stav schválení Field Service nastaven na *Null*.
+ Pokud je stav schválení nákupní objednávky v Supply Chain Management nastaven na *Schváleno*, *Probíhá externí kontrola*, *Potvrzeno* nebo *Dokončeno*, stav schválení nákupní objednávky Field Service bude nastaven na *Schváleno*.
+ Pokud je stav schválení nákupní objednávky v Supply Chain Management nastaven na *Zamítnuto*, stav schválení nákupní objednávky Field Service bude nastaven na *Zamítnuto*.
+ Pokud se stav záhlaví dokumentu v Supply Chain Management změní na *Otevřená objednávka (zpětná objednávka)* a stav nákupní objednávky Field Service je *Koncept* nebo *Zrušeno*, stav nákupní objednávky ve Field Service se změní na *Odesláno*.
+ Pokud se stav záhlaví dokumentu v Supply Chain Management změní na *Zrušeno* a ve Field Service nejsou žádné produkty příjmu nákupní objednávky spojené s nákupní objednávkou (prostřednictvím produktů nákupní objednávky), stav systému Field Service se nastaví na *Zrušeno*.
+ Pokud je stav řádku nákupní objednávky v Supply Chain Management *Zrušeno*, je stav produktu objednávky ve Field Service nastaven na *Zrušeno*. Kromě toho, pokud se změní stav řádku nákupní objednávky v Supply Chain Management ze *Zrušeno* na *Zpětná objednávka*, je stav položky produktu nákupní objednávky ve Field Service nastaven na *čekající*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Synchronizace na vyžádání s nákupem v Supply Chain Management

Supply Chain Management zahrnuje údaje o nákupu, které zpracovávají obchodní dohody, slevy a další scénáře, které se spoléhají na sekundární procesy v Supply Chain Management. Nákupní stroj používá složitá pravidla k určení nejvhodnější ceny pro danou nabídku nákupní objednávku. Když používáte duální zápis, data se ne vždy synchronizují napříč dvěma prostředími, zejména ve scénářích, kde byl řádek vytvořen nebo aktualizován z Dataverse a může spustit následné procesy v Supply Chain Management.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Synchronizace dat nákupu ze Supply Chain Management

1. V Dataverse, jděte na **Sklad \> Nákupní objednávka**.
2. Volbou **Nová** vytvořte novou nákupní objednávku nebo řádek pro existující nákupní objednávku.
3. Z nákupní objednávky nebo řádku nákupní objednávky.
4. V podokně akcí vyberte **Synchronizovat**.

Všechny sloupce z Dataverse a Field Service, které sdílí Supply Chain Management, jsou synchronizovány.

Zde jsou situace, kdy můžete použít funkci **Sync** :

- Pokud provedete několik po sobě jdoucích změn ve stejném řádku z Dataverse, spusťte funkci **Synchronizace**.
- Pokud si nejste jisti, zda může být změna druhou po sobě jdoucí změnou Dataverse, mohlo by mít smysl spustit funkci **Synchronizace**.
- Pokud se zobrazí chybová zpráva o aktualizaci hodnoty ze Supply Chain Management, spusťte funkci **Synchronizace** a poté zkuste aktualizaci zopakovat v Dataverse.

## <a name="cancelling-the-posting-process"></a>Zrušení procesu zaúčtování

Pokud je proces zaúčtování příjmu produktu zrušen během zpracování, pak by duální zápis mohl vytvořit řádek příjmu produktu Dataverse, ale nevytvářejte řádek příjmu produktu v Supply Chain Management. K této situaci dochází, protože duální zápis nepodporuje distribuované transakce.

## <a name="templates"></a>Šablony

Následující šablony jsou k dispozici pro integraci dokumentů souvisejících se zakázkami.

| Správa dodavatelsko-odběratelského řetězce | Field Service | popis |
|---|---|---|
| Záhlaví nákupní objednávky V2 | msdyn\_Purchaseorders | Tato tabulka obsahuje sloupce, které představují záhlaví nákupní objednávky. |
| Entita řádku nákupní objednávky | msdyn\_PurchaseOrderProducts | Tato tabulka obsahuje řádky, které představují řádky nákupní objednávky. Číslo produktu je použito k synchronizaci. To identifikuje produkt jako skladovou jednotku (SKU), včetně rozměrů produktu. Další informace o integraci produktu s Dataverse najdete v části [Jednotná zkušenost s produktem](product-mapping.md). |
| Záhlaví příjemky produktů | msdyn\_purchaseorderreceipts | Tato tabulka obsahuje záhlaví příjemky produktu, které se vytvoří při zaúčtování příjemky produktu v Supply Chain Management. |
| Řádek příjemky produktu | msdyn\_purchaseorderreceiptproducts | Tato tabulka obsahuje řádky příjemky produktu, které se vytvoří při zaúčtování příjemky produktu v Supply Chain Management. |
| Obnovitelně odstraněná entita řádku nákupní objednávky | msdyn\_purchaseorderproducts | Tato tabulka obsahuje informace o řádcích nákupní objednávky, které jsou vymazány. Řádek nákupní objednávky v Supply Chain Management lze vymazat pouze tehdy, když je nákupní objednávka potvrzena nebo schválena, pokud je zapnuto řízení změn. Řádek existuje v databázi Supply Chain Management a je označen jako **Je odstraněno**. Protože Dataverse nemá koncept měkkého mazání, je důležité, aby byly tyto informace synchronizovány s Dataverse. Tímto způsobem lze automaticky mazat řádky, které jsou v Supply Chain Management odstraněny z Dataverse. V tomto případě se logika pro odstranění řádku z Dataverse nachází v Supply Chain Management Extended. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/productreceiptheader-msdyn-purchaseorderreceipts.md)]

[!include [Currency](includes/productreceiptline-msdyn-purchaseorderreceiptproducts.md)]

[!include [Currency](includes/purchaseorderheadersv2-msdyn-purchaseorders.md)]

[!include [Currency](includes/purchaseorderlinesoftdeletedtable-msdyn-purchaseorderproducts.md)]

[!include [Currency](includes/purchaseorderlinetable-msdyn-purchaseorderproducts.md)]
