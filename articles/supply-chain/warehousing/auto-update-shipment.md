---
title: Automatické aktualizace dodávek
description: V tomto tématu je uveden přehled funkcí, které poskytují automatické aktualizace dodávek.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1f75e9421ab9cac0b62e1cdee17ecf74796783cc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001217"
---
# <a name="shipment-auto-updates"></a>Automatické aktualizace dodávek

[!include [banner](../includes/banner.md)]

Funkce Automatické aktualizace dodávky automaticky aktualizuje množství (zvyšuje i snižuje) na řádku vytížení, který je spojen s dodávkou, poté, co bylo vytížení uvolněno do skladu. Tato funkce zůstane zapnuta, dokud není řádek vytížení na dodávce nebo vytížení zpracován ve vlně. Při použití aktualizace objednávek mohou automaticky proudit do skladu bez nutnosti ručního zásahu do doby, než bude vytvořena práce ve skladu.

Není-li použita funkce automatické aktualizace dodávky, množství pouze automaticky snižuje tok do doby, než bude vytvořena práce ve skladu. Uživatelé musí řádky aktualizovat nebo odstranit ručně a musí tyto řádky znovu uvolnit, pokud dojde ke zvýšení množství objednávky nebo k přidání nových řádků objednávky. Díky funkci automatické dodávky aktualizací mohou podniky bezproblémově poskytovat aktualizace do skladu, aniž by se museli obávat, že související dodávky a vytížení neodráží aktualizace řádku objednávky.

Funkce automatické aktualizace dodávky se použije pro řádky prodejní objednávky i pro řádky převodního příkazu a je zapnuta pro určitý sklad. Z toho vyplývá, že společnosti mohou použít různé zásady dodávek s automatickou aktualizací v různých skladech tak, jak to vyžadují. Ve výchozím nastavení je pro všechny sklady, které používají procesy správy skladu, použita zásada automaticky aktualizovat dodávky pro snížení množství. Je-li použito toto výchozí nastavení, množství automaticky snižuje tok do dodávky a vytížení do doby, než bude vytvořena práce ve skladu. Toto chování se podobá chování, které bylo použito před zavedením funkce Automatické aktualizace dodávky.

## <a name="main-elements-of-the-functionality"></a>Hlavní prvky funkce

Funkce Automatické aktualizace dodávky spoléhá především na stav dodávky k určení, zda se má při provedení změny v řádku prodejní objednávky nebo v řádku převodního příkazu změnit množství na řádku vytížení. Dále spoléhá především na stav dodávky k určení, kdy by měl být do existujícího vytížení automaticky přidán nový řádek. Pokud je stav dodávky nastaven na **Zařazeno do vlny** nebo vyšší, nedojde k automatické aktualizaci.

Stav vlny se také bere v úvahu pro automatické aktualizace. Pokud má vlna, která souvisí s řádkem břemene, stav **Pozastaveno**, **Zpracování**, **Uvolněno**, **Vyskladněno** nebo **Expedováno**, pokud se uživatel pokusí snížit množství na řádku vytížení (prostřednictvím snížení množství na řádku prodejní objednávky nebo na řádku převodního příkazu) se zobrazí následující chybová zpráva: „Rezervace nelze odebrat, protože je vytvořena práce, která závisí na rezervacích“. Pokud má vlna jeden z dříve zmíněných stavů vlny, pokud se uživatel pokusí nepřímo zvýšit množství řádku vytížení pomocí zvýšení množství na řádku prodejní objednávky nebo řádku převodního příkazu, množství na řádku nákladů nebude automaticky zvýšeno. Pokud má vlna jeden z dříve zmíněných stavů vlny, pokud se uživatel pokusí nepřímo zvýšit množství řádku vytížení pomocí zvýšení množství na řádku prodejní objednávky nebo řádku převodního příkazu, množství na řádku nákladů nebude automaticky zvýšeno.

## <a name="scenarios"></a>Scénáře

Funkce automatické aktualizace dodávky podporuje čtyři scénáře: přidání nového řádku objednávky, zvýšení množství v řádku objednávky, snížení množství na řádku objednávky a odstranění řádku objednávky.

- **Přidat nový řádek objednávky** – Pokud je pole **Automaticky aktualizovat dodávku** na pevné záložce **Sklad** na stránce **Sklady** (**Správa skladů \> Nastavení \> Sklad \> Sklady**) nastaveno na **Vždy**, pokud u objednávky existuje dodávka a je přidán nový řádek do prodejné objednávky nebo převodního příkazu poté, co už bylo vytvořeno vytížení pro danou prodejní objednávku, existující vytížení se nebude aktualizovat. Je vytvořen nový řádek vytížení, který nemá odkaz na existující vytížení, a je přidružen k existující dodávce. Nový řádek je přidán do vytížení a uvolněn.
- **Zvýšit množství v řádku objednávky** – když je pole **Automaticky aktualizovat dodávku** nastaveno na **Vždy**, pokud pro objednávku existuje dodávka a množství na existujícím řádku prodejní objednávky nebo řádku převodního příkazu se zvyšuje po vytvoření vytížení pro prodejní objednávku, řádek vytížení se zvýší o stejné množství, jako řádek objednávky. Pokud byla uvolněno vytížení, ale nebyla vytvořena žádná práce, řádek vytížení bude zvýšen o stejné množství jako řádek objednávky.
- **Snížit množství na řádku objednávky** – Pokud je pole **Automaticky aktualizovat dodávku** nastaveno na hodnotu **Vždy** nebo **Při snížení množství**, pokud pro objednávku existuje dodávka a množství na existujícím řádku prodejní objednávky nebo řádku převodního příkazu je snížen poté, co již bylo vytvořeno vytížení pro prodejní objednávku, množství na přiřazeném řádku vytížení se aktualizuje, aby bylo spárováno, pokud množství na řádku vytížení již není rovno nebo nižší než nové množství na řádku objednávky. V takovém případě nebude řádek vytížení ovlivněn. Pokud bylo uvolněno vytížení, ale nebyla vytvořena žádná práce, množství na přiřazeném řádku vytížení se aktualizuje pro spárování, pokud množství na řádku vytížení již není rovno nebo nižší než nové množství na řádku objednávky. V takovém případě je řádek vytížení ovlivněn.
- **Odebrat řádek objednávky** – když je pole **Automaticky aktualizovat dodávku** nastaveno na hodnotu **Vždy** nebo na **Při snížení množství**, pokud se uživatel pokusí odebrat řádek objednávky, pro který existuje řádek vytížení, zobrazí se chybová zpráva.

## <a name="example-scenario"></a>Příklad

V tomto scénáři musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Zapnutí funkce Automatické aktualizace dodávky

Chcete-li zapnout funkci Automatické aktualizace dodávky, postupujte dle následujících kroků.

1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
2. Vyberte sklad **24**.
3. Na pevné záložce **Sklad** v poli **Automaticky aktualizovat dodávku** změňte hodnotu z **Při snížení množství** na **Vždy**.

Po změně hodnoty na **Vždy** se jakékoliv zvýšení nebo snížení množství na řádcích prodejní objednávky a v řádcích převodního příkazu a jakékoli přidání nových řádků odrazí v dodávkách a vytíženích pro vybraný sklad, a to za předchozích uvedených omezení aktualizací.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Změňte šablonu vlny tak, aby nebyly automaticky zpracovány řádky vytížení.

Chcete-li konfigurovat šablonu vlny tak, aby automaticky nezpracovávala řádky naložení, postupujte podle následujících kroků.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
2. Vyberte šablonu vlny **Vychozí dodávka 24**.
3. Vyberte možnost **Upravit**.
4. Na pevné záložce **Obecné** nastavte možnost **Automatická tvorba vlny** na **Ano** a ujistěte se, že žádná další možnost není nastavena na **Ne**.

Je důležité, aby v rámci procesu vytvoření vlny nebyla automaticky vytvořena a uvolněna žádná práce. Po vytvoření práce související s řádkem vytížení, který byl vytvořen pro řádek prodejní objednávky, nebude po změně množství na řádku prodejní objednávky automaticky aktualizován řádek vytížení.

### <a name="create-a-sales-order"></a>Vytvořit prodejní objednávku

Chcete-li vytvořit prodejní objednávku, postupujte následujícím způsobem.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
2. Vyberte odběratele **US-003**.
3. Vytvořte řádek pro číslo položky **A0001**.
4. Zadejte množství **10**. (Ujistěte se, že používáte sklad **24**.)
5. Zvolte **Uložit**.
6. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.** Je vytvořena dodávka a vlna.

Protože jste změnili šablonu vlny v předchozím postupu, není vytvořeno žádné vytížení ani práce. Stav dodávky je **Otevřeno** a stav vlny je **Vytvořeno**.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Snižte množství na řádku prodejní objednávky

Chcete-li snížit množství na řádku prodejní objednávky, postupujte takto.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
2. Vyberte prodejní objednávku, kterou jste právě uvolnili do skladu.
3. Vyberte řádek prodejní objednávky. V poli **Množství** změňte hodnotu z **10** na **8**.
4. V řádku prodejní objednávky vyberte možnost **Sklad \> Podrobnosti dodávky**. Na stránce **Podrobnosti dodávky** na pevné záložce **Řádky vytížení** množství odráží změnu na řádku prodejní objednávky.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Zvyšte množství na řádku prodejní objednávky

Chcete-li zvýšit množství na řádku prodejní objednávky, postupujte takto.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
2. Vyberte prodejní objednávku, kterou jste před tím uvolnili do skladu.
3. Změňte množství řádku z **8** na **12**.
4. Zvolte **Uložit**.
5. Vraťte se zpět na stránku **Všechny prodejní objednávky** a znovu vyberte prodejní objednávku.
5. V podokně akcí na kartě **Sklad** ve skupině **Související informace** vyberte **Podrobnosti dodávky**. Na stránce **Podrobnosti dodávky** na pevné záložce **Řádky vytížení** množství odráží změnu na řádku prodejní objednávky.

Ačkoliv bylo množství na řádku vytížení zvýšeno z 8 na 12, zůstalo rezervováno pouze osm položek, pokud není zpnuta automatická rezervace. Vzhledem k tomu, že množství přidané do existující dodávky nebylo rezervováno, pokud je v tomto okamžiku vlna zpracována, bez rezervace, bude práce vytvořena pouze pro množství, které již bylo rezervováno.

> [!NOTE]
> Pokud je sníženo množství na řádku objednávky, množství na řádku vytížení nebude ovlivněno, pokud se již rovná nebo je menší než nové množství na řádku objednávky. Po zvýšení množství na řádku objednávky se řádek vytížení zvýší o stejné množství jako řádek objednávky. Pokud se množství na řádku objednávky liší od množství na řádku vytížení, zůstane rozdíl v nabídce.

### <a name="add-a-sales-order-line"></a>Přidání řádku prodejní objednávky

Pro přidání řádku prodejní objednávky postupujte následujícím způsobem.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
2. Vyberte prodejní objednávku, kterou jste před tím uvolnili do skladu.
3. Vytvořte řádek pro číslo položky **A0002**.
4. Do pole **Množství** zadejte **10**. (Ujistěte se, že používáte sklad **24**.) Nový řádek je automaticky přidán do existující dodávky.
5. Zvolte **Uložit**.
6. Vraťte se zpět na stránku **Všechny prodejní objednávky** a znovu vyberte prodejní objednávku.
7. V podokně akcí na kartě **Sklad** ve skupině **Související informace** vyberte **Podrobnosti dodávky**. Na kartě **Podrobnosti dodávky** na pevné záložce **Řádky vytížení** si povšimněte druhého řádku vytížení.

Protože řádek prodejní objednávky, který jste právě přidali do existující dodávky, nebyl rezervován, pokud je v tomto okamžiku vlna zpracována, bude práce vytvořena pouze pro množství na prvním řádku prodejní objednávky a na prvním řádku vytížení.

### <a name="process-a-wave"></a>Zpracovat vlnu

Chcete-li zpracovat vlnu, postupujte následovně.

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
2. Vyberte dříve vytvořenou vlnu.
3. V podokně akcí na kartě **Vlna** ve skupině **Vlna** zvolte **Zpracovat**.

Vlna se zpracuje a vytvoří práci pro rezervovaná množství na řádcích vytížení. Stav dodávky se aktualizuje z **Otevřeno** na **Zařazeno do vlny**. Protože stav dodávky je aktualizován na **Zařazeno do vlny**, veškeré změny, ke kterým dochází, například snížení nebo zvýšení v množství řádku nebo přidání nových řádků do prodejní objednávky, neovlivní stávající řádky nákladů, které jsou přidruženy k dodávce zařazené do vlny.

Pokud má dodávka stav **Zařazeno do vlny** nebo vyšší, aktualizace množství na řádku prodejní objednávky se neodrazí ani se neověřuje podle řádku vytížení, který je přiřazen k dodávce. Změny množství na řádku vytížení musí být provedeny přímo na řádku vytížení.

Ověření je provedeno po vytvoření práce pro řádek vytížení a po provedení rezervace. Snížení množství na řádku prodejní objednávky se ověří podle rezervace řádku práce.
