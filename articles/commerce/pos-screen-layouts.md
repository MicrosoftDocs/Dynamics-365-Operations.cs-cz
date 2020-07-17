---
title: Vizuální konfigurace uživatelského rozhraní POS
description: Toto téma obsahuje informace o rozložení obrazovky pro prostředí POS aplikace Dynamics 365 Commerce.
author: boycezhu
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycezhu
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a037c8514d7838b3a4797f21b3ef3f6d5736e840
ms.sourcegitcommit: f7294160d18f15cb762c24f2459b4f0887c37541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/25/2020
ms.locfileid: "3505627"
---
# <a name="pos-user-interface-visual-configurations"></a>Vizuální konfigurace uživatelského rozhraní POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Uživatelské rozhraní Retail POS Microsoft Dynamics 365 Commerce lze konfigurovat pomocí kombinace vizuálních profilů a rozložení obrazovky, které jsou přiřazeny k obchodům, registračním pokladnám a uživatelům. V tomto tématu jsou uvedeny další informace o těchto konfiguračních možnostech.

Následující obrázek ukazuje vztahy mezi různými entitami, které tvoří konfigurovatelné aspekty uživatelského rozhraní POS.

![Entity rozložení obrazovky POS](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Vizuální profil

Vizuální profily jsou přiřazeny registrům a určují vizuální prvky, které jsou specifické pro registrační pokladnu a sdílené mezi uživateli. Každý uživatel, který se přihlásí k registrační pokladně, bude mít stejný motiv, rozvržení, barvy a obrázky.

![Uvítací obrazovka POS se světlým motivem](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![Obrazovka transakcí POS s tmavým motivem](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Číslo profilu** -číslo profilu je jedinečný identifikátor vizuálního profilu.
- **Popis** -můžete zadat smysluplný název, který vám pomůže identifikovat správný profil pro danou situaci.
- **Motiv** - můžete zvolit mezi **Světlým** a **Tmavým** motivem aplikace. Motiv ovlivní barvu písma a pozadí napříč aplikací.
- **Barva zvýraznění** -barva zvýraznění v celém POS slouží k odlišení nebo zvýraznění konkrétních vizuálních prvků, jako jsou dlaždice, příkazová tlačítka a hypertextové odkazy. Tyto prvky typicky slouží k provádění akcí.
- **Barva záhlaví** – lze konfigurovat barvu záhlaví stránky podle požadavků maloobchodníka týkajících se značky.
- **Schéma písem** – můžete vybrat mezi **standardním** a **velkým** schématem písem. Schéma písem má vliv na velikost písma v celé aplikaci. Implicitně je vybráno nastavení **Standardní**.
- **Vždy zobrazit popisky čárových aplikací** – je-li tato možnost zapnuta, text popisku se vždy zobrazí pod tlačítky na panelu aplikace.
- **Rozvržení** – můžete vybrat mezi rozvržením **uprostřed** a **vpravo**. Rozvržení ovlivňuje zarovnání přihlašovacího pole v přihlašovací obrazovce. Implicitně je vybráno nastavení **Uprostřed**.
- **Zobrazit datum a čas** – je-li tato možnost zapnuta, bude aktuální datum a čas zobrazeno v záhlaví POS a na přihlašovací obrazovce.
- **Klávesnice** – můžete vybrat **výchozí nastavení na klávesnici OS** a **zobrazit číselnou klávesnici**, která určuje výchozí klávesnici, která se použije pro vstup na přihlašovací obrazovce. Tato číselná klávesnice je virtuální klávesnicí, která se používá především pro dotyková zařízení. Výchozí nastavení je **výchozí nastavení na klávesnici OS**.
- **Obrázek loga** – můžete určit obrázek loga, který se zobrazí v přihlašovací obrazovce. Doporučujeme použít obrázek, který má průhledné pozadí. Velikost obrázků je třeba uchovávat co nejmenší, protože ukládání a načítání velkých souborů může mít vliv na chování a výkon aplikace.
- **Pozadí přihlašování** - můžete zadat obrázek pozadí pro přihlašovací obrazovku. Velikost souboru obrázku na pozadí by měla být co nejmenší.
- **Pozadí** - můžete určit obrázek pozadí, který bude použit namísto plné barvy motivu v celé aplikaci. Pokud se jedná o obrázky pozadí pro přihlašovací obrazovku, měla by být velikost souboru udržována co nejmenší.

> [!NOTE]
> Na přihlašovací obrazovce v kompaktním zobrazení se nezobrazuje **správné** rozvržení a datum a čas.

## <a name="screen-layouts"></a>Rozložení obrazovky

Konfigurace rozložení obrazovky určují akce, obsah a umístění ovládacích prvků uživatelského rozhraní na **ǘodní** obrazovce POS a obrazovce **Transakce**.

![Zobrazení rozložení obrazovky POS](../commerce/media/POS-Screen-Layout-View.png)

- **Úvodní obrazovka** - ve většině případů je uvítací obrazovka stránka, kterou uživatelé uvidí při prvním přihlášení do POS. Úvodní obrazovka může obsahovat obrázek značky a mřížky tlačítek, které poskytují přístup k operacím POS. Obvykle jsou na této obrazovce umístěny operace, které nejsou specifické pro aktuální transakci.

    ![Úvodní obrazovka POS](../commerce/media/POS-Welcome-Screen.png)

- **Obrazovka Transakce** - obrazovka **Transakce** je hlavní obrazovka v POS pro zpracování prodejních transakcí a objednávek. Obsah a rozložení se konfigurují pomocí návrháře rozložení obrazovky.

    ![Obrazovka POS pro transakce](../commerce/media/POS-Transaction-Screen.png)

- **Výchozí úvodní obrazovka** - někteří maloobchodníci mají raději, když pokladník po přihlášení přejde přímo na obrazovku **Transakce**. Nastavení **výchozí úvodní obrazovky** umožňuje určit výchozí obrazovku, která se zobrazí po přihlášení pro každé rozvržení obrazovky.

### <a name="assignment"></a>Přiřazení

Rozložení obrazovky mohou být přiřazena na úrovni obchodu, registrační pokladny nebo uživatele. Přiřazení uživatele přepíše přiřazení registrační pokladny a obchodu a přiřazení registrační pokladny přepíše přiřazení obchodu. V jednoduchém případě, kde všichni uživatelé používají stejné rozvržení bez ohledu na registr nebo roli, lze rozvržení obrazovky nastavit pouze na úrovni obchodu. V případech, kde konkrétní registrační pokladny nebo uživatelé vyžadují speciální rozložení, lze jim je přiřadit.

### <a name="layout-sizes"></a>Velikosti rozvržení

Většina aspektů uživatelského rozhraní POS je responzivní a rozložení se automaticky mění a upravuje podle velikosti a orientace obrazovky. Obrazovku POS **Transakce** je třeba nakonfigurovat pro každé rozlišení obrazovky, které se očekává.

Při spuštění aplikace POS automaticky zvolí nejbližší velikost rozložení nakonfigurovanou pro zařízení. Rozložení obrazovky může také obsahovat konfigurace pro režimy na šířku a na výšku, stejně jako pro zařízení s plnou velikostí a kompaktní zařízení. Uživatelé mohou být přiřazeni k jednomu rozvržení obrazovky, které bude fungovat v různých velikostech a formátech používaných v obchodě.

![Velikosti rozvržení POS](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Název** – můžete zadat popisný název pro identifikaci velikosti obrazovky.
- **Typ rozložení** – POS aplikace může zobrazit své uživatelské rozhraní v různých režimech k dosažení optimálního uživatelského prostředí na daném zařízení.

    - **Moderní POS - úplné** -úplná rozložení jsou obvykle nejvhodnější pro větší displeje, jako jsou monitory a tablety. Můžete vybrat prvky uživatelského rozhraní, které mají být zahrnuty, určit velikost a umístění těchto prvků a nakonfigurovat jejich podrobné vlastnosti. Plná rozložení podporují konfigurace na výšku a na šířku.
    - **Modern POS - kompaktní -** - kompaktní rozložení jsou obvykle nejvhodnější pro telefony a malé tablety. Možnosti návrhu jsou omezeny pro kompaktní zařízení. Můžete konfigurovat sloupce a pole pro účtenky a panely součtů.

- **Výška a šířka** – tyto hodnoty představují účinnou velikost obrazovky (v pixelech), které se pro rozložení očekává. Mějte na paměti, že některé operační systémy používají přizpůsobení pro displeje s vysokým rozlišením.

> [!TIP]
> Velikost rozvržení vyžadovanou pro obrazovku POS můžete zjistit zobrazením rozlišení v aplikaci. Spusťte POS a přejděte na **Nastavení \> Informace o relaci**. POS zobrazí rozvržení obrazovky, které je aktuálně načteno, velikost rozvržení a rozlišení okna aplikace.

![Stránka s informacemi o relaci POS zobrazující rozvržení aktuálně načtené obrazovky, velikost rozvržení a rozlišení okna aplikace.](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Mřížky tlačítek

Pro každou velikost rozvržení v rozvržení obrazovky můžete konfigurovat a přiřadit mřížky tlačítek pro úvodní obrazovku POS a obraovku **Transakce**. Mřížky tlačítek pro úvodní obrazovku jsou automaticky rozloženy zleva doprava od nejnižšího čísla (úvodní obrazovka 1) k nejvyššímu číslu.

V úplném rozložení POS je umístění mřížky tlačítek určeno v návrháři rozložení obrazovky.

V kompaktním rozvržení POS jsou mřížky tlačítek automaticky rozvrženy odshora dolů, od nejnižšího čísla (obrazovka transakcí 1) k nejvyššímu číslu. Lze k nim přistoupit v nabídce **Akce**.

![Mřížky tlačítek kompaktního rozvržení](../commerce/media/Compact-View-Button-Grids.png)

### <a name="images"></a>Obrázky

Pro každou velikost rozvržení na obrazovce rozvržění můžete určit obrázky, které mají být zahrnuty v uživatelském rozhraní POS. V úplném rozložení POS lze zadat jeden obrázek pro úvodní obrazovku. Tento obrázek se zobrazí jako první prvek uživatelského rozhraní vlevo. Na obrazovce **Transakce** lze použít obrázky jako obrázky karty nebo jako logo. Kompaktní rozvržení POS tyto obrázky nepoužívá.

### <a name="screen-layout-designer"></a>Návrhář rozložení obrazovky

Návrhář rozložení obrazovky jevám umožní konfigurovat různé aspekty obrazovky POS **Transakce** pro každou velikost rozvržení, jak v režimu na výšku, tak na šířku, a úplné i kompaktní rozvržení. Návrhář rozvržení obrazovky používá technologii nasazení ClickOnce ke stažení, instalaci a spuštění nejnovější verze aplikace pokaždé, když k ní uživatel přistupuje. Je nutné zkontrolovat požadavky prohlížeče pro ClickOnce. Některé prohlížeče, jako je například Google Chrome, požadují rozšíření.

> [!IMPORTANT]
> Je nutné konfigurovat rozložení obrazovky pro každou velikost rozvržení definovanou a používanou v POS.

### <a name="full-layout-designer"></a>Návrhář úplného rozložení

Návrhář úplného rozložení umožňuje uživatelům přetáhnout ovladací prvky uživatelského rozhraní na obrazovku POS **Transakce** a nakonfigurovat nastavení těchto prvků.

![Návrhář úplného rozložení POS (režim na šířku)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Importovat rozvržení/Exportovat rozvržení** – můžete exportovat a importovat návrhy rozvržení obrazovky POS jako soubory XML, tak, abyste je mohli znovu použít a sdílet je napříč prostředími. Je důležité, abyste importovali návrhy rozvržení pro správné velikosti rozvržení. V opačném případě se prvky uživatelského rozhraní nemusí správně vejít na obrazovku.
- **Na šířku/na výšku** – pokud POS zařízení umoňuje uživateli přepínat mezi režimem na šířku a výšku, je nutné definovat rozložení obrazovky pro každý režim. POS automaticky zjistí otočení obrazovky a zobrazí správné rozvržení.
- **Mřížka rozložení** – návrhář rozložení POS používá 4pixelovou mřížku. Ovládací prvky uživatelského rozhraní se „přichytí“ k mřížce, aby vám pomohly správně zarovnat obsah.
- **Zvětšení návrháře** – můžete zvětšit nebo změnšit zobrazení návrháře pro lepší zobrazení obsahu na POS obrazovce. Tato funkce je užitečná, když se rozlišení obrazovky na POS značně liší od rozlišení obrazovky, která se používá v návrháři.
- **Zobrazit/skrýt navigační panel** – pro úplné rozvržení POS můžete zvolit, zda bude levý navigační panel zobrazen na obrazovce **Transakce**. Tato funkce je užitečná pro displeje s nižším rozlišení. Chcete-li nastavit viditelnost, klikněte pravým tlačítkem myši na navigační panel v návrháři a zaškrtněte nebo odškrtněte políčko **Vždy viditelné**. Pokud je navigační panel skrytý, mohou k němu uživatelé POS přistupovat pomocí nabídky v levém horním rohu.

    ![Zobrazit/skrýt navigační panel](../commerce/media/Navigation-Bar.PNG)

- **Ovládací prvky POS** – návrhář rozložení POS podporuje ovládací prvky. Můžete konfigurovat mnoho ovládacích prvků pravým tlačítkem myši a použitím nabídky zástupců.

    ![Ovládací prvky uživatelského rozhraní POS](../commerce/media/POS-UI-Controls.png)

    - **Číselná klávesnice** - číselná klávesnice je hlavním mechanismem pro uživatelské vstupy na obrazovce POS **Transakce**. Ovládací prvek můžete nakonfigurovat tak, aby se zobrazovala úplná číselná klávesnice. Tato možnost je ideální pro zařízení s dotykovou obrazovkou. Rovněž je možné ji nakonfigurovat tak, aby se zobrazovalo pouze zadávací pole. V takovém případě slouží pro zadávání vstupů fyzické klávesnice. Nastavení číselné klávesnice jsou k dispozici v úplném rozložení. U kompaktního rozvržení se vždy zobrazí úplná číselná klávesnice na obrazovce **Transakce**.
    - **Souhrnný panel** - souhrnný panel lze konfigurovat v jednom nebo dvou sloupcích k zobrazení hodnot, jako je počet řádků, částka slevy, poplatky, souhrn a daně. Kompaktní rozvržení podporuje pouze jeden sloupec.
    - **Panel příjmu** - Panel příjmu obsahuje prodejní řádky, řádky platby a doručení informace o produktech a službách, které jsou zpracovávány v POS. Můžete určit sloupce, šířku a umístění. V kompaktním rozvržení také můžete nakonfigurovat doplňující informace, které se zobrazí na řádku pod hlavním řádkem.
    - **Karta zákazníka** - tato karta zobrazuje informace o zákazníkovi , který je přidružený k aktuální transakci. Kartu zákazníka můžete nakonfigurovat tak, aby zobrazovala nebo skrývala další informace.
    - **Ovládací prvek karty** - ovládací prvek karty můžete přidat k rozvržení obrazovky a poté do ní přidat další ovládací prvky, jako je číselná klávesnice, karta zákazníka nebo tlačítka mřížky. Ovládací prvek karty je kontejner, který vám umožňuje přidat více obsahu na obrazovku. Ovládací prvek karty je dostupný pouze pro úplná rozložení.
    - **Obrázek** - můžete použít ovládací prvek obrázku k zobrazení loga obchodu nebo jiného obrázku značky na obrazovce **Transakce**. Ovládací prvek obrázku je dostupný pouze v úplném rozložení.
    - **Doporučené produkty** - Je-li nakonfigurován doporučený ovládací prvek produktu pro prostředí, zobrazuje návrhy produktu založené na strojovém učení.
    - **Vlastní ovládací prvek**- vlastní ovládací prvek funguje jako zástupce v rozvržení obrazovky a umožňuje vám rezervovat místo pro vlastní obsah. Vlastní ovládací prvek je dostupný pouze pro úplné rozložení.

### <a name="compact-layout-designer"></a>Návrhář kompaktního rozložení

Stejně jako návrhář úplného rozvržení vám návrhář kompaktního rozložení umožňuje nakonfigurovat rozvržení obrazovky POS pro telefony a malé tablety. Nicméně v tomto případě je samotné rozložení pevné. Můžete konfigurovat ovládací prvky v roložení pravým tlačítkem myši a použitím nabídky zástupců. Nelze však použít operace uchopení a přetažení pro další obsah.

![Návrhář kompaktního rozložení](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Návrhář mřížky tlačítek

Návrhář mřížky tlačítek vám umožňuje konfigurovat mřížky tlačítek, které lze použít na úvodní obrazovce POS a obrazovce **Transakce** pro úplné a kompaktní rozvržení. Stejnou mřížku tlačítek lze použít napříč rozvrženími a typy rozvržení. Stejně jako návrhář rozvržení obrazovky používá návrhář mřížky tlačítek technologii nasazení ClickOnce ke stažení, instalaci a spuštění nejnovější verze aplikace pokaždé, když k ní uživatel přistupuje. Je nutné zkontrolovat požadavky prohlížeče pro ClickOnce. Některé prohlížeče, jako je například Google Chrome, požadují rozšíření.

![Návrhář mřížky tlačítek](../commerce/media/Button-Grid-Designer.png)

- **Nové tlačítko** – kliknutím přidátet nové tlačítko na mřížku tlačítek. Ve výchozím nastavení se nová tlačítka zobrazí v levém horním rohu mřížky. Můžete však uspořádat tlačítka jejich přetažením do rozvržení.

    > [!IMPORTANT]
    > Obsah mřížky tlačítek se může překrývat. Když uspořádáte tlačítka, ujistěte se, že neskrývají ostatní tlačítka.

- **Nový návrh** – kliknutím automaticky nastavte rozložení mřížky tlačítek určením počtu tlačítek na řádek a sloupec.
- **Vlastnosti tlačítek** – vlastnosti tlačítka lze konfigurovat tak, že kliknete pravým tlačítkem myši na tlačítko a použijee nabídku zástpců.

    > [!IMPORTANT]
    > Některá nastavení mřížky tlačítek se vztahují pouze k Enterprise POS, nikoliv k Modern POS nebo Cloud POS.

    ![Vlastnosti tlačítka mřížky tlačítek](../commerce/media/Button-grid-button-properties.png)

    - **Akce** – v seznamu použitelných POS operací vyberte operaci, která bude vyvolána při kliknutí na tlačítko v POS.

        Ohledně seznamu podporovaných operací POS nahlédněte do části [Online a offline operace pokladních míst (POS)](pos-operations.md).

    - **Parametry akce** – některé operace POS používají další parametry, když jsou vyvolány. Například pro operaci přidání produktů mohou uživatelé určit produkt, který má být přidán.
    - **Text na tlačítku** - zadejte text zobrazený na tlačítku v POS.
    - **Skrýt text na tlačítkách** – zaškrtněte toto políčko pro skrytí nebo zobrazení textu tlačítka. Text na tlačítkách je často skrytý u malých tlačítek, která jsou zobrazena pouze jako ikona.
    - **Popis tlačítka** – zadejte dodatečný text nápovědy, který se zobrazí, když na tlačítko ukážete myší.
    - **Velikost ve sloupcích/velikost v řádcích** – můžete určit výšku a šířku tlačítka.

        ![Velikosti tlačítek POS v řádcích a sloupcích](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Vlastní písma** – když vyberete zaškrtávací políčko **Povolit vlastní písmo pro POS**, můžete zadat jiné písmo, než je součástí výchozího systému POS.
    - **Vlastní motiv** – standardně používají tlačítka POS barvu zvýraznění z vizuálního profilu. Když vyberete zaškrtávací políčko **Použít vlastní motiv**, můžete určit další barvy.

        > [!NOTE]
        > Modern POS a Cloud POS používají pouze hodnoty **Barva pozadí** a **Barva písma**.

    - **Obrázek tlačítka** – tlačítka mohou obsahovat obrázky a ikony. Vyberte z obrázků dostupných pod možností **Maloobchod a velkoobchod \> Nastavení kanálu \> Nastavení POS \> POS \> Obrázky**.

![Příklad mřížky tlačítek v POS](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Další zdroje

[Instalace návrháře rozložení pokladního místa Retail (POS)](install-pos-layout-designer.md)
