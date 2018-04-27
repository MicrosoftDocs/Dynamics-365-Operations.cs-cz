---
title: "Zásady nákupu"
description: "V tomto článku jsou informace o zásadách nákupu. Zásady nákupu jsou soubor pravidel řídících proces nákupní žádanky. Zásady nákupu umožňují správcům zásobování implementovat strategie zásobování vytvořením struktury zásad, které jsou v souladu se strategickými požadavky organizace na nákupy."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 11614
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 675a7a8b0da228e789ee37ca8fe1d0c0ea01c283
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="purchasing-policies"></a>Zásady nákupu

[!INCLUDE [banner](../includes/banner.md)]

V tomto článku jsou informace o zásadách nákupu. Zásady nákupu jsou soubor pravidel řídících proces nákupní žádanky. Zásady nákupu umožňují správcům zásobování implementovat strategie zásobování vytvořením struktury zásad, které jsou v souladu se strategickými požadavky organizace na nákupy.

Zásady nákupu obsahují sadu pravidel zásad. Když definujete pravidlo zásad, nejprve vyberte typ pravidla zásad. Poté vytvoříte pravidlo pro typ pravidla definováním nastavení, počáteční datum a koncové datum pro pravidlo.  

Například správce vytvoří zásady, vybere typ pravidla **zásad katalogu** a poté do zásad přidá pravidlo zásad katalogu. Toto pravidlo zásad katalogu určuje, že katalog Adventure musí být použit pro interní zásobování. Poté, co zásady nákupu jsou přidruženy k dané organizaci, zaměstnancům organizace se zobrazí katalog Adventure při vytváření žádanek.

## <a name="assigning-policies-to-organizations"></a>Přiřadit zásad organizacím
Předtím, než zásada začne platit, musí být přidružena k organizaci. Zásady nákupu jsou přidruženy k účelům hierarchie **interní kontroly zásobování**. Proto zásady nákupu platí pouze pro organizace v hierarchiích, které mají jako účel hierarchie **interní kontrolu zásobování**. Můžete také vybrat organizace z plochého seznamu právnických osob v tabulce CompanyInfo. Tyto právnické osoby v rámci zásady patří do kategorie "Společnosti".

## <a name="determining-which-rule-to-apply"></a>Zjišťování, jaké pravidlo použít
V závislosti na konfiguraci zásad nakupování může uživatele v organizaci ovlivnit více pravidel. Následující příklady ilustrují různými způsoby, jak můžete konfigurovat zásady nákupu a určit způsob použití zásad dojde-li k transakci.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Příklad 1: Jednoduchá konfigurace zásad nákupu

Pro organizace, které jsou malé a méně složité, lze nastavit zásady nákupu podle právnické osoby a lze použít pouze organizační hierarchii společnosti.  

Pro společnost Fabrikam, malý podnik, se v celé organizaci budou trochu lišit nákupní požadavky. Pravidla nákupu se liší pouze mezi organizacemi právnických osob. Například zaměstnanci v Fabrikam (Kanada) a zaměstnanci Fabrikam (USA) nakupují zboží a služby z jiných katalogů a od různých dodavatelů. Proto společnost Fabrikam nastavuje své zásady nákupu na úrovni právnické osoby.  

Společnost Fabrikam vytváří dvě zásady nákupu. Zásady A platí pro právnickou osobu v USA, 1111. Zásady B platí pro právnickou osobu v Kanadě, 2222. Pokud zaměstnanec v právnické osobě 1111 vytvoří nákupní žádanku, pravidla zásad jsou odvozena ze zásad A. Například katalog produktů, který vidí zaměstnanec, je zadán v pravidle zásad katalogu pro zásady A.  

Pokud zaměstnanec v právnické osobě 2222 vytvoří nákupní žádanku, pravidla zásad jsou odvozena ze zásad B.  

**Poznámka:** Pokud zaměstnanec právnické osoby 1111 nakupuje položku jménem zaměstnance právnické osoby 2222, použijí se pravidla zásad, která jsou zadána pro právnickou osobu 2222 (to znamená zásady pravidla ze zásady B).

### <a name="example-2-complex-purchasing-policy-configuration"></a>Příklad 2: Složitá konfigurace zásad nákupu

V předchozím příkladě byla definována všechna pravidla nákupu v jedné organizační hierarchii, organizační hierarchií společnosti. Komplexní organizace však může definovat zásady pro více organizačních hierarchií.  


Společnost Contoso je velká společnost, která vyžaduje komplexní pravidla nákupu k řízení zpracování žádanek. Společnost Contoso definovala pravidla pro dvě různé organizační hierarchie: Řízení oddělení a globální kontroly.  

Zásada 123 je definována pro oddělení organizační hierarchie pro prodejní oddělení pro prodej ve Velké Británii. V zásadách 123 pravidlo kontroly nákupní žádanky určuje, že musí být vynucena omezení pro minimální objednané množství. V tomto pravidle je vybrána možnost **Vynutit omezení minimálního množství objednávky**.  

Zásada 456 je definována pro organizační hierarchii globální kontroly nákupu pro prodejní a marketingové oddělení. V zásadách 456 pravidlo kontroly nákupní žádanky neurčuje, že musí být vynucena omezení pro minimální objednané množství. V tomto pravidle není vybrána možnost **Vynutit omezení minimálního množství objednávky**.  

Stanislav pracuje v prodejním oddělení pro prodej ve Velké Británii v kanceláři společnosti Contoso pro oblast Spojené království. Pro jeho oddělení platí zásady pro organizační hierarchii Řízení oddělení a globální kontroly. Když Stanislav vytvoří nákupní žádanku, musí v systému určit, kterou zásadu chce použít. Správce systému nastaví potřebné parametry zásad nákupu a určí, zda zásady nákupu musí být podle priority použity v následujícím pořadí:

1.  Řízení globální kontroly
2.  Oddělení
3.  Společnosti

Zásada 456 je tedy použita pro nákupní žádanku, kterou Stanislav vytvoří a u dané nákupní žádanky nebude vyžadováno žádné minimální množství objednávky.

## <a name="policy-rules"></a>Pravidla zásad
### <a name="catalog-policy-rule"></a>Pravidlo zásad katalogu

Pravidlo zásad katalogu určuje, jaký zásobovací katalog se zobrazí uživatelům při vytváření nákupních žádanek. Pokud uživateli bylo uděleno oprávnění k objednávce produktů za jiného uživatele, žádanka použije pravidlo zásad katalogu, které je definováno pro právnickou osobu žadatele a provozní jednotku pro určení, který katalog se zobrazí. Dříve než můžete definovat pravidlo zásad katalogu, musíte vytvořit katalog zásobování a publikovat ho.

### <a name="category-access-policy-rule"></a>Pravidlo zásad přístupu ke kategorii

Pravidlo zásad přístupu ke kategorii určuje, které kategorie uživatelů mají přístup při vytváření nákupních žádanek. Není-li určeno žádné pravidlo, všechny kategorie zásobování lze přidat do nákupního žádanky.

1.  Vyberte možnost **Zahrnout nadřazené pravidlo** a použijte pravidlo zásad přístupu ke kategorii nadřazené organizace na kategorii.
2.  V podokně **Dostupné kategorie** vyberte kategorie, na které se pravidlo vztahuje. Pokud vyberete kategorii, jsou do seznamu **Vybrané kategorie** přidány také všechny kategorie, které jsou v hierarchii výše.
3.  Vyberte možnost **Zahrnout podkategorie**, chcete-li pravidlo použít na všechny podkategorie vybrané kategorie.

### <a name="category-policy-rule"></a>Pravidlo zásad kategorie

Pravidla zásad kategorií definují, jak pro každou kategorii mohou uživatelé vybírat dodavatele. Definuje také požadavky pro procesy příjmu a fakturace.

### <a name="re-approval-rule-for-purchase-orders"></a>Pravidlo opětovného schválení pro nákupní objednávky

Pravidlo opětovného schválení je volitelné pravidlo, které definuje kritéria pro vyžadování opětovného schválení při změně nákupní objednávky. Vybraná pole jsou vyhodnocena ve workflow prodejní objednávky, je- li ve workflow podmínka nastavena na „Vyžaduje opětovné schválení nákupní objednávky“.

> [!NOTE]
> Rozúčtování bude vynulováno vždy při změně schválené nákupní objednávky s povolenou funkcí Správa změn. Proto byste měli mít na vědomí, že pokud se chcete vyhnout opětovnému schvalování nákupní objednávky při změně některých polí, NEMĚLO by být pro opětovné schválení zahrnuto pole Změna rozúčtování. 

### <a name="purchase-requisition-rfq-rule"></a>Pravidlo požadavku na nabídku nákupní žádanky

Pravidlo požadavku na nabídku nákupní žádanky definujte kritéria pro vyžadování požadavku na nabídku (RFQ) pro řádek nákupní žádanky. Pokud řádek splňuje podmínky, na řádku požadavku se zobrazí údaj „neformální RFQ“ nebo „formální RFQ“.

### <a name="purchase-requisition-control-rule"></a>Pravidlo řízení nákupní žádanky

Pravidlo řízení nákupní žádanky je volitelné pravidlo. Při vytváření pravidla tohoto typu lze na různých kartách nastavit možnosti:

-   Na kartě **Odeslání workflowu** můžete konfigurovat pole, které je třeba zadat na řádku žádanky pro odeslání žádanky ke schválení, pokud je účelem žádanky **Spotřeba**.
-   Na kartě **Množství objednávek** lze konfigurovat pole, která jsou za určitých podmínek požadována nákupní žádanku. Můžete také vynutit objednané množství.
-   Na kartě **Data** můžete nastavit, zda je datum účetnictví stejné jako požadované datum.
-   Na kartě **Adresa** můžete definovat, zda uživatel může vytvářet nové adresy v systému k použití do nákupního žádanky.

### <a name="requisition-purpose-rule"></a>Pravidlo účelu žádanky

Pravidlo účelu žádanky je volitelné pravidlo, která určuje typ účelu žádanky, který je povolený pro určitou právnickou osobu. Není-li v tomto pravidle určen jiný účel, žádanky při jejich vytváření mají automaticky účel **Spotřeba**.

### <a name="replenishment-category-access-policy-rule"></a>Pravidlo zásad přístupu ke kategorii doplnění

Pravidlo doplnění kategorie zásad přístupu je volitelné pravidlo určující produkty, které jsou k dispozici k uspokojení poptávku žádanky pro určitou právnickou osobu, pokud je účelem žádanky **Doplnění**.

### <a name="replenishment-control-rule"></a>Pravidlo řízení doplnění

Pravidlo řízení doplnění je volitelné pravidlo definující pole, které je třeba zadat na řádku žádanky k odeslání ke schválení, pokud je účelem žádanky požadavku **doplnění**.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Pravidlo vytvoření nákupní objednávky a konsolidace poptávky

Pravidlo pro tvorbu nákupní objednávky a konsolidaci poptávky definuje zásady pravidla, které se mají použít při generování nákupní objednávky ze schválené nákupní žádanky. Při vytváření pravidla tohoto typu lze na různých kartách nastavit možnosti:

-   Na kartě **Rozdělení nákupní objednávky** můžete definovat kritéria pro rozdělení řádků nákupní žádanky do samostatných nákupních objednávek.
-   Na kartě **Převod cen/slev** můžete při vytvoření nákupní objednávky definovat při přepočítání dohodu o ceně:
    -   **Pouze pokud neexistuje žádná obchodní smlouva** – Ceny a slevy jsou přeneseny z nákupní žádanky pouze v případě, že neexistuje žádná platná obchodní smlouva nebo základní cena. Pokud u položky nebo dodavatele existuje obchodní smlouva nebo základní cena, ceny a slevy jsou přepočítány podle obchodní smlouvy nebo základní ceny a použity v nákupní objednávce. Pokud není stanoveno jinak, toto je výchozí chování.
    -   **Vždy** – Ceny a slevy jsou vždy převedeny z nákupních žádanek.

    Můžete také povolit žadateli změnit způsobu předání ceny a slevy pro jednotlivé řádky nákupní žádanky, bez ohledu na pravidlo přenosu ceny/slevy, které je definováno. Vyberte možnost **Povolit ručně přepsat řádek nákupní žádanky**, pokud chcete povolit tuto funkci.
-   Na kartě **Převod popisu položky** je možné přenést popis položky z žádanky, pokud pochází z požadavku nabídky.
-   Na kartě **Tolerance ceny** můžete definovat pravidla používaná ke směrování schválené nákupní žádanky zpět do procesu kontroly při zvýšení cen zboží v zásobovacím katalogu. Nastavte maximální částku, kterou můžete zvětšit čistou částku řádkové položky na nákupní žádance mezi okamžikem schválení nákupní žádanky a časem, kdy je vytvořena nákupní objednávka. Čistá částka se vypočte podle následujícího vzorce: : (\[množství × (jednotková cena – sleva) ÷ cenová jednotka\] + vedlejší náklady na nákup) × (100 – % slevy) ÷ 100 řádků nákupní žádanky, přesahující toleranci ceny, kterou jste nastavili, jsou pro ruční zpracování pozdrženy. Pravidla, která konfigurujete na kartě **Zpracování chyb**, určují způsob zpracování požadavků řádků nákupní žádanky.
-   Na kartě **Zpracování chyb** můžete nakonfigurovat pravidlo zpracování, které platí pro nákupní žádanku, pokud se nezdaří ověřování při vytvoření nákupní objednávky z důvodu chyby dodavatele nebo chyby tolerance ceny. Vyberte některou z následujících možností:
    -   **Žádná akce** – řádky nákupní žádanky zůstávají na stránce **Uvolnit schválené nákupní žádanky**. Stav řádků nákupní žádanky zůstane nastaven na hodnotu **Schváleno**. Chyby však musí být vyřešeny před možností vygenerovat nákupní objednávku pro řádky nákupní žádanky.
    -   **Zrušit řádek vybrané nákupní žádanky** – řádky nákupní žádanky jsou zrušeny. Žadatel může vytvořit novou nákupní žádanku pro zrušené řádky, pokud chce stále požádat o položky řádků.
    -   **Vytvoření nového řádku nákupní žádanky** – řádky nákupní žádanky jsou zrušeny. Jsou pak generovány nové nákupní žádanky obsahující řádky nákupní žádanky, jejichž ověření se nezdařilo. Po vygenerování nových nákupních žádanek budou mít stav **Koncept**. Tyto nákupní žádanky lze znovu odeslat ke kontrole po ověření vyřešených chyb. Zpracovatel řádků nákupní žádanky je upozorněn, že řádky byly zrušeny a že byly generovány nové nákupní žádanky pro řádky nákupní žádanky, které selhaly.
-   Na kartě **Ruční vytvoření nákupní objednávky** můžete definovat parametry, které určují, zda nákupní žádanka musí být ručně zpracována nebo zda ji lze automaticky převést na nákupní objednávku. Parametry lze použít na položky interního katalogu, položky externího katalogu nebo položky mimo katalog. Vyberte některou z následujících možností:
    -   **Ručně vytvářet nákupní objednávky** – vytvářejte ručně nákupní objednávky pro všechny nákupní žádanky.
    -   **Automaticky vytvářet nákupní objednávky** – vytvářejte automaticky nákupní objednávky pro všechny schválené nákupní žádanky. Žádné nákupní žádanky nejsou uchovávány pro ruční vytvoření nákupní objednávky.
    -   **Automaticky vytvářet nákupní objednávky kromě případů, které splňují tyto podmínky** – vytvářejte ručně nákupní objednávky pro nákupní žádanky, které splňují kritéria, které definujete. Všechny ostatní nákupního žádanky, které jsou schváleny, jsou automaticky převedeny na nákupní objednávky. Vyberete-li možnost **Automaticky vytvářet nákupní objednávky kromě případů, které splňují tyto podmínky**, můžete přidat kategorie zásobování a dodavatelů k určení, které schválené řádky nákupní žádanky jsou drženy pro ruční zpracování. Tuto možnost lze použít na položky interního katalogu, položky externího katalogu a položky mimo katalog. Po výběru kategorie zásobování jsou vybrány také všechny podkategorie pro danou kategorii zásobování. Vyberte možnost **Vše** pro určitý typ řádku nákupní žádanky pro uložení všech řádků tohoto typu řádku pro ruční zpracování.

    Pokud chcete nákupní objednávky automaticky generovat ze schválených nákupních žádanek při spuštění dávkové úlohy pro spouštění generování nákupní objednávky, zaškrtněte políčko **Spustit automatické vytvoření nákupních objednávek jako dávkovou úlohu**. Tato možnost se vztahuje pouze na nákupní žádanky, které nevyžadují ruční zpracování. Spuštěním automatického generování nákupní objednávky jako dávkové úlohy můžete naplánovat tuto aktivitu v době, kdy jsou zdroje méně vytíženy. Pokud je na řádku nákupní žádanky vybrána možnost **Požadována záloha**, vyberte možnost **Když je žádanka nastavena pro zálohu** pro blokování schválených nákupních žádanek k ručnímu zpracování. Nákupní žádanky, které jsou drženy pro ruční zpracování, lze filtrovat tak, že můžete zobrazit pouze ty řádky nákupních žádanek, které vyžadují platbu předem.
-   Na kartě **Konsolidace poptávky** můžete definovat parametry, které určují, zda nákupních řádky, které jsou zpracovány ručně, lze považovat pro konsolidaci nákupních žádanek. Parametry lze použít na položky interního katalogu, položky externího katalogu nebo položky mimo katalog. Vyberte některou z následujících možností:
    -   **Nepovolit konsolidaci poptávky** – nárok na konsolidaci poptávky nemají žádné schválené řádky nákupních žádanek. Tato možnost je vybrána ve výchozím nastavení a platí pouze pro řádky nákupních žádanek, které vyžadují ruční zpracování pro vytvoření nákupní objednávky.
    -   **Vždy povolit konsolidaci poptávky** – nárok na konsolidaci poptávky mají všechny schválené řádky nákupních žádanek. **Poznámka:** vyberete-li možnost **Vždy povolit konsolidaci poptávky** na kartě **Konsolidace poptávky**, ale vyberte možnost **Automatické vytváření nákupních objednávek** na kartě **Ruční vytvoření nákupní objednávky**, budou všechny nákupní žádanky pozdrženy pro ruční zpracování.
    -   **Povolit konsolidaci poptávky za těchto podmínek** – definujte kritéria, která určují, zda schválené řádky nákupních žádanek mají nárok na konsolidaci poptávky. Pro každý typ řádku nákupní žádanky můžete nastavit kritéria podle kategorie zásobování a dodavatele. Pokud vyberete možnost **Povolit konsolidaci poptávky za těchto podmínek**, můžete nastavit kritéria podle kategorie zásobování a dodavatele pro každý typ řádku nákupní žádanky. Po výběru kategorie zásobování jsou vybrány také všechny podkategorie pro danou kategorii zásobování. Vyberete-li možnost **Vše** pro konkrétní typ řádku, jsou všechny řádky nákupní žádanky tohoto typu řádku způsobilé pro konsolidaci poptávky.





