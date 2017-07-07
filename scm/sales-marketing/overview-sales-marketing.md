---
title: Prodej a marketing
description: "Modul prodeje a marketingu můžete používat k získávání, ukládání a používání různých druhů v průběhu prodeje. Mezi tato data patří původní prodejní iniciativy, budoucí následné akce a dodatečné prodeje."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: dddcc764bb11540b8207350c463d1adb2533e1c0
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017


---

# <a name="sales-and-marketing"></a>Prodej a marketing

[!include[banner](../includes/banner.md)]


Modul prodeje a marketingu můžete používat k získávání, ukládání a používání různých druhů v průběhu prodeje. Mezi tato data patří původní prodejní iniciativy, budoucí následné akce a dodatečné prodeje.

<a name="marketing"></a>Marketing
---------

Můžete používat marketingové kampaně a aktivity pro hledání potenciálních zákazníků a vytváření vztahů s nimi tak, aby se počáteční interakce mohly rozvíjet do prodejních vztahů. Následující vývojový diagram znázorňuje obchodní proces marketingu. [![Obchodní proces pro marketing](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Vztahy

V okně Prodej a marketing může v různých situacích dojít k počátečním interakcích s potenciálními zákazníky. Například můžete objevit potenciálního zákazníka, zatímco se účastníte veletrhu, nebo naleznete potenciálního zákazníka poté, co vaše organizace realizuje hromadnou poštovní kampaň. Je velmi důležité porozumět toku u entity strany, než se tato strana stane zákazníkem. Následující obrázek znázorňuje vztahy toku u entity tak, jak se z potenciálního zákazníka stává skutečný zákazník. [![SalesandMarketing01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampaně

Kampaň cílí na kontakty od potenciálních zákazníků, zájemce, příležitosti a zákazníky, kteří byli vybráni k účasti v kampani. V aplikaci Microsoft Dynamics 365 for Finance and Operations můžete vytvořit několik typů kampaní, jako je telemarketing, poštovní kampaň a e-mailové kampaně a maximalizovat tak potenciál zákazníků. V průběhu kampaně a jak budete přijímat kladné odpovědi, můžete začít s prodejem u těchto příjemců, kteří na kampaň odpověděli kladně.

## <a name="sales"></a>Prodeje
Prodejní funkce můžete použít k vytvoření nabídek, návaznému a křížovému prodeji u nových a stávajících zákazníků, pro vytváření prodejních objednávek a vytváření prodejních faktur pro zákazníky. Následující vývojový diagram znázorňuje obchodní proces pro prodej. [![Obchodní proces pro prodej](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Prodejní nabídky

Prodejní nabídky můžete vytvořit pro zpřístupnění nabídky zboží nebo služeb které budete zákazníkům poskytovat. Zákazník může požádat o cenovou nabídku, nebo můžete vytvořit nabídku jako odpověď na požadavek od existujících nebo potenciálních zákazníků. Když zákazník odsouhlasí prodejní nabídku, můžete ji převést na prodejní objednávku.

### <a name="up-sellcross-sell"></a>Návazný/křížový prodej

Návazný a křížový prodej jsou techniky pro prodej výrobků, když je zadána objednávka pro zákazníka. U návazného prodeje bude navržen jiný produkt namísto aktuálního produktu. U křížového prodeje bude navržen produkt navíc k aktuálnímu produktu. Při nastavování seznamů produktů můžete vytvořit zvláštní pravidla, která označují, kdy by měl být produkt navržen jako produkt pro návazný či křížový prodej.

### <a name="sales-orders"></a>Prodejní objednávky

Při vytváření nové prodejní objednávky je třeba vybrat typ prodejní objednávky, kterou chcete vytvořit. Existuje pět možností. **Poznámka:** po vytvoření prodejní objednávky můžete typ objednávky libovolně změnit, s výjimkou typu **Požadavky položky** v případě, že má prodejní objednávka stav **Dodáno**.

| Typ prodejní objednávky  | Popis                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Deník           | Tento typ slouží jako koncept pro prodejní objednávku. Tento typ nemá žádný vliv na množství zásob a negeneruje položkové transakce.                                                                                                                                                                    |
| Předplatné      | Tento typ se používá pro stálé objednávky. Když se objednávka vyfakturuje, stav objednávky se automaticky nastaví na otevřenou objednávku. Fakturované dodané množství a zbývající dodávky se aktualizují. Tento typ prodejní objednávky nelze použít, pokud používáte funkci pro správu skladu. |
| Prodejní objednávka       | Tento typ použijte, když zákazník umístí nebo potvrdí objednávku.                                                                                                                                                                                                                                        |
| Vratka    | Tento typ se používá, když odběratel vrátí položku. Číslo vráceného zboží (číslo RMA) bude přiřazeno automaticky.                                                                                                                                                                                            |
| Požadavky na položky | Tento typ se vytvoří automaticky, kdy vytvoříte prodej položky pomocí projektu.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Prodejní smlouvy

Prodejní smlouva je smlouva, která zaváže odběratele k nákupu produktu v určitém množství nebo stanovené částce za určitý čas výměnou za zvláštní ceny nebo slevy. Ceny a slevy prodejní smlouvy přepíší všechny ceny a slevy, uvedené ve všech obchodních smlouvách, které případně existují. Prodejní smlouva je platná pro definované období. Požadované datum expedice určené pro prodej na stránce **Prodejní objednávka** by mělo být z platného období. Prodejní smlouva je ve výchozím nastavení blokována. Můžete objednat z prodejní smlouvy pouze v případě, že je nastavena na hodnotu **Účinné**.

### <a name="backorders"></a>Doobjednávky

Při zadávání a ověřování objednávek může být před dokončením prodeje nezbytné zajistit správu doobjednávek a výjimek. Doobjednávky jsou buď nákupní objednávky, které ještě nebyly dodány od dodavatele, nebo prodejní objednávky, které ještě nebyly dodány zákazníkovi. Je důležité, abyste se zpětnými objednávkami zabývali podrobněji. Pokud se například zpozdí produkty od dodavatele, bude asi nezbytné změnit termín dodání pro odběratele a rovněž je o zpoždění informovat. Doobjednávky můžete zobrazit podle zboží, zákazníka nebo dodavatele.

#### <a name="viewing-backorders-by-item"></a>Zobrazení doobjednávek podle položky

Při zobrazení doobjednávek podle položky se lze podrobně zabývat očekávaným tokem transakcí vztahujícího se ke konkrétní položce. Můžete například zkontrolovat následující informace:

-   Počet prodejních objednávek zadaných na položku.
-   Jestli stále není doručeno zboží od dodavatele.
-   Zda by mělo být doobjednáno více zboží, aby všechny prodejní objednávky bylo možné realizovat včas.

Provedením této kontroly může odpovídat na požadavky od zákazníků o načasování dodání zboží. Navíc lze určit prioritu zpětných prodejních objednávek a také položky snadno rozdělit mezi objednávky.

#### <a name="viewing-backorders-by-customer"></a>Zobrazení doobjednávek podle odběratelů

Přehled zpětných objednávek podle odběratele umožňuje zobrazení statusu zbývajících objednávek odběratele. Tato kontrola je užitečná, když musíte reagovat na zákazníky, kteří čekají na zboží, které bylo zpožděno.

#### <a name="viewing-backorders-by-vendor"></a>Zobrazení objednávky podle dodavatele

Při zobrazení doobjednávek podle dodavatele můžete sledovat chybějící dodávky a očekávané termíny doručení. Tato kontrola pomáhá určit prioritu doobjednávek, když jsou produkty doručeny od dodavatelů a je nutné vydat prodejní objednávky pro dodávku.

### <a name="invoices"></a>Faktury

Během prodejního procesu můžete vytvořit tři typy faktur:

-   Faktura odběratele
-   Volné faktury
-   Proforma faktura

#### <a name="customer-invoice"></a>Faktura odběratele

Faktura odběratele je vyúčtování, které organizace předává odběrateli ve spojitosti s prodejem. Tento druh faktury odběratele vychází z prodejní objednávky, která obsahuje záhlaví a jeden nebo více řádků pro zboží nebo služby. Faktura odběratele představuje konec cyklu prodejní objednávky, dodacího listu a prodejní faktury.  

Můžete zaúčtovat a vytisknout jednu fakturu odběratele založenou na prodejní objednávce nebo na dodacím listu a datu. K dispozici je vám také zaúčtování a tisk více faktur odběratele společně podle dodacích listů a dat. Při zaúčtování jedné faktury odběratele pomocí prodejní objednávky se množství v poli **Fakturovaný zůstatek** u každé položky aktualizováno celkovým fakturovaným množstvím z vybrané prodejní objednávky.  

Pokud bude množství **Fakturovaný zůstatek** i množství **Zbývá dodat** pro všechny položky na prodejní objednávce nulové (0), stav prodejní objednávky se změní na hodnotu **Fakturováno**. Pokud množství v některém z polí není nulové, stav prodejní objednávky zůstane nezměněn a lze pro ni zadat další faktury. Pokud chcete zaúčtovat a vytisknout jednu nebo více faktur odběratele podle dodacích listů, musíte již mít zaúčtován alespoň jeden dodací listu pro každou prodejní objednávku. Faktura odběratele je založena na těchto dodacích listech a odráží na nich uvedená množství.  

Můžete vytvořit fakturu odběratele založenou na položkách řádku dodacího listu, které byly odeslány k určitému datu, a to i když všechny položky pro určitou prodejní objednávku nebyly dosud odeslány. To lze provést například v situaci, kdy daná právnická osoba vystavuje každému odběrateli jednu fakturu měsíčně, která zahrnuje všechny dodávky za daný měsíc. Každý dodací list odpovídá částečné nebo úplné dodávce položek na prodejní objednávce.  

Při zaúčtování faktury bude množství **Zůstatek faktury** pro každou položku aktualizováno o souhrn dodaných množství z vybraných dodacích listů. Pokud bude množství **Zůstatek faktury** a množství **Zbývá dodat** pro všechny položky na prodejní objednávce nulové (0), stav prodejní objednávky se změní na hodnotu **Fakturováno**. Pokud množství není nulové, stav prodejní objednávky zůstane nezměněn a lze pro ni zadat další faktury. Skladové transakce budou aktualizovány s použitím čísla faktury a stav na řádku prodejní objednávky se změní na hodnotu **Fakturováno**.

#### <a name="free-text-invoice"></a>Volné faktury

Faktura s volným textem představuje fakturu, která není připojena k prodejní objednávce. Obsahují řádky objednávky zahrnující účty hlavní knihy, libovolné textové popisy a částku prodeje. Číslo položky v tomto druhu faktury nelze zadat. Je však nutné zadat příslušné informace o DPH. Hlavní účet pro prodej je vyznačen na každém řádku faktury. Zůstatek odběratele je zaúčtovány do souhrnného účtu z účetního profil, který se používá pro volnou fakturu.

#### <a name="pro-forma-invoice"></a>Proforma faktura

Proforma faktura je faktura připravená jako odhad skutečných částek faktury před zaúčtováním faktury. Lze ji vytisknout pro fakturu odběratele nebo volnou fakturu.




