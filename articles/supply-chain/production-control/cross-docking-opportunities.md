---
title: "Cross docking z výrobních příkazů na výstupní překladiště"
description: "Toto téma popisuje, jak spravovat zpracování cross docking materiálu, který je vykazován jako dokončený z výrobní linky do výstupního překladiště."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCrossDockOpportunityPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 62194012cfbe101d19e9de3254afb004da79a562
ms.contentlocale: cs-cz
ms.lasthandoff: 03/07/2018

---

# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Cross docking z výrobních příkazů na výstupní překladiště

[!include[banner](../includes/banner.md)]

Toto téma popisuje, jak spravovat zpracování cross docking materiálu, který je vykazován jako dokončený z výrobní linky do výstupního překladiště.

<a name="introduction"></a>Úvod
------------

Cross docking z výroby do výstupního skladového místa je relevantní pro výrobce, kteří produkují velké množství a v ideálním případě chtějí expedovat dokončené produkt při jejich prohlášení za dokončené z výrobních linek. Účelem je dodat produkty do distribučních center, které se fyzicky nacházejí blízko poptávky odběratele, namísto vytváření zásob na výrobním pracovišti.

V případě, že neexistuje okamžitá poptávka po produktu, musí být produkt umístěn do skladových míst na výrobním pracovišti. Tento proces se nazývá také *příležitostný cross-docking*, což znamená, že pokud existuje poptávka po dodání produktu, je třeba tuto příležitost využít, namísto odkládání produktu do interního úložiště.

Následující příklad ukazuje tři odchylky toku, který začíná na konci výrobní linky (2).

Produkt je vykázaný jako dokončený do výstupního místa výroby (3) a řidič vysokozdvižného vozíku na tomto místě vyzvedne paletu (3).

-   Pokud existuje plánovaná aktivita (6) pro přepravu produktu z výroby (1) do distribučního centra (7), bude řidič vysokozdvižného vozíku nasměrován systémem k umístění palety k nákladové bráně (4).
-   Pokud je k nákladové bráně již přiřazen přívěs, řidič nákladního automobilu bude nasměrován k přímému naložení výrobku na přívěs.
-   Pokud neexistuje žádná plánovaná aktivita pro převod produktu, řidič vysokozdvižného vozíku bude nasměrován umístit produkt v interním skladu (5).

[![příležitostný cross docking](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Konfigurace cross dockingu
Proces cross dockingu se konfiguruje v **zásadách práce**. Zásady práce obsahují typ pracovního příkazu, umístění a produkt. V následujícím příkladu je cross docking nakonfigurovaný pro produkt X a skladové místo Y.

#### <a name="work-order-types"></a>Typy pořadí pracovních činností

-   Typ pracovního příkazu: Výdej dokončeného zboží
-   Metoda vytvoření práce: Cross docking
-   Název zásad pro cross docking: Objednávky transferu

#### <a name="inventory-locations"></a>Skladová místa

-   Sklad: 51
-   Skladové místo: Y

#### <a name="products"></a>Produkty

-   Číslo položky: X

Cross docking v současné době může být konfigurován pouze pro dva typy pracovních příkazů:

-   Výdej dokončeného zboží
-   Vyskladnění vedlejšího produktu

V **zásadě cross dockingu** definujete, jaké typy dokumentů jsou použitelné pro cross docking. V současné době je jediný podporovaný typ dokumentu **Objednávka transferu**. Následující příklad ukazuje konfiguraci zásady cross dockingu.

### <a name="cross-docking-policy-name-transfer-order"></a>Název zásady cross dockingu: Objednávka transferu

-   Pořadové číslo: 10
 -   Typ pracovního příkazu: Vydání transferu
-   Poptávka po cross dockingu vyžaduje skladové místo: Ne
-   Strategie cross dockingu: Datum a čas

### <a name="sequence-number"></a>Pořadové číslo

**Pořadové číslo** označuje prioritu typu dokumentu. V současné době je jediný podporovaný typ **Objednávka transferu**. Číselná řada bude tedy relevantní pouze v případě, když bude podporováno více typů pracovních příkazů.

### <a name="cross-docking-policy"></a>Zásada cross dockingu

Zásada cross dockingu rovněž nastavuje zásadu pro určení priority poptávky po objednávce transferu. Například pokud existuje více objednávek transferu pro stejný výrobek, naplánované datum a čas, které jsou nastavené na nákladu a přiřazené k objednávce transferu, určují prioritu mezi objednávkami. Plánované datum a čas lze nastavit přímo na nákladu, nebo je lze nastavit na **plánu události** přiřazeném k nákladu. Stanovení priorit je určeno strategií cross dockingu. V současné době existuje pouze jedna strategie: **Datum a čas**.

### <a name="cross-docking-demand-requires-location"></a>Poptávka po cross dockingu vyžaduje skladové místo

V zásadách cross dockingu můžete nastavit kritérium pro vyžádání, aby objednávky transferu měli přiřazené skladové místo a tím mohly být oprávněné pro cross docking. Toto kritérium se nastavuje v poli **Poptávka po cross dockingu vyžaduje skladové místo**. Skladové místo na plánu událostí přiřazené k nákladu se používá jako konečné místo pro zboží využívající cross docking. Konečné skladové místo pro zboží, které právě využívá cross dockingu, je určeno směrnicí skladového místa pro **Vydání transferu** pro typ pracovního příkazu **Vložit**. Může pro vás být užitečné nastavit pole **Poptávka po cross dockingu vyžaduje skladové místo** v situaci, kdy by dokončené zboží mělo využít cross dockingu pouze tehdy, je-li k nákladové bráně přiřazen přívěs. V tomto scénáři je zboží přesunuto do přívěsu přímo z výrobní linky. Při přiřazení přívěsu k nákladové bráně přiřadí uživatel skladové místo k plánu událostí a tím učiní skladové místo použitelným pro cross docking. Následující části vás provedou dvěma příklady.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>Scénář 1 – Cross docking z výroby až po objednávky transferu

Po vykázání produktu jako dokončeného na výrobní lince je produkt dopraven k nákladové bráně, kde je naložen na nákladní vozidlo a přepraven do distribučního centra. Použijte společnost USMF.

1.  Povolte novou číselnou řadu pro cross docking. Přejděte na stránku **Číselné řady** a vyberte tlačítko **Generovat**. Procesem vás provede průvodce.
2.  Vytvořte zásadu cross dockingu. Přejděte na stránku **Zásady cross dockingu** a vytvořte novou zásadu s názvem **Cross docking pro objednávku transferu**. Všimněte si, že typ pracovního příkazu, který můžete vybrat, je **Vydání transferu**, a jediná dostupná strategie cross dockingu je **Datum a čas**.
3.  Vytvoření zásadu práce. Přejděte na stránku **Zásady práce** a vytvořte novou zásadu práce s názvem **Cross Dock L0101**.
4.  Nastavte náklady tak, aby se vytvářely pro objednávky transferu automaticky. V parametrech skladu nastavte náklady tak, aby se vytvářely automaticky při vytváření objednávek transferu. Náklad je předpokladem pro vytváření objednávky transferu oprávněné pro cross docking.
5.  Nastavte mapování nákladu položek. Přejděte na stránku **Mapování nákladu položek** a nastavte standardní šablonu nákladu na skupinu položek **CarAudio**. Toto mapování automaticky při vytvoření objednávky transferu vloží šablonu nákladu.
6.  Vytvořte převodní příkaz. Vytvořte objednávku transferu pro položku číslo L0101. Množství = 20.
7.  Uvolněte objednávku transferu z pracovní plochy plánování nákladu. Na kartě **Expedice** vyberte položku nabídky pro pracovní plochu plánování nákladu a v nabídce **Uvolnit** řádku nákladu vyberte **Uvolnit do skladu**. Nyní existuje otevřený řádek vlny typu **Objednávka transferu** pro objednávku transferu.
8.  Vytvořte výrobní zakázku. Přejděte na stránku seznamu **Výrobní zakázka** a vytvořte výrobní zakázku pro produkt L0101. Množství = 20. Odhadněte a zahajte výrobní zakázku. Všimněte si, že pole **Zaúčtovat výdejku** zůstává nastaveno na **Ne**.
9.  Vykázání jako dokončené z mobilního zařízení. Přejděte k portálu mobilního zařízení a vyberte položku nabídky **Ohlásit jako dokončené a odložit**. Nyní vykažte jako dokončené L0101 z mobilního zařízení. Množství = 10. Všimněte si, že skladové místo je **BAYDOOR**. Toto skladové místo naleznete ze směrnice skladového místa **Vydání transferu** pro typ pracovního příkazu **Vložit**. Všimněte si též, že práce typu **Vydání transferu** byla vytvořena a dokončena. Přejděte na podrobnosti práce objednávky transferu, chcete-li ověřit práci.
10. Nyní vykažte dalších 10 kusů z mobilního zařízení. Všimněte si, že skladové místo je opět **BAYDOOR**. Všimněte si též, že nová práce typu **Vydání transferu** byla vytvořena pro těchto 10 kusů.
11. Nyní se pokuste spustit o 20 kusů více na výrobní zakázce a poté zkuste vykázat 20 kusů jako dokončených pomocí ručního zařízení. Tentokrát se jako skladové místo nabídne **LP-001**. Toto umístění se nalezne ze směrnice skladového místa pro **Výdej dokončeného zboží**. Tato směrnice skladového místa se používá, protože neexistuje žádná příležitost pro cross docking. Objednávka transferu pro LP-001 byla zcela splněna dvěma aktivitami cross dockingu v kroku 9 a 10. Všimněte si, že práce typu **Výdej dokončeného zboží** byla vytvořena a zpracována.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Scénář 2 - Cross docking z výroby k objednávce transferu s plánem události

Poté, co je výrobek vykázán jako dokončený na výrobní lince, je přepraven na místo nákladové brány, které je identifikováno plánem událostí pro místo nákladové brány. Použijte společnost USMF.

1.  Změňte zásadu cross dockingu. Změňte zásadu cross dockingu, kterou jste vytvořili ve scénáři 1 volbou zaškrtávacího políčka **Poptávka po cross dockingu vyžaduje skladové místo**.
2.  Vytvořit novou objednávku transferu.
3.  Otevřete **Pracovní plocha plánování nákladu**.
4.  Z pracovní plochy plánování nákladu přejděte do části **Náklad** a zvolte **Plán událostí** v nabídce **Přeprava** k vytvoření nového plánu události. Upozorňujeme, že plán události má odkaz na objednávku transferu v poli **Číslo objednávky**. V poli **Plánované počáteční datum a čas v umístěníě** můžete nastavit datum a čas pro událost. Toto datum a čas se použije se při stanovení priorit poptávky po cross dockingu během během procesu cross dockingu. Datum a čas, které jste nastavili do tohoto pole, aktualizují pole **Datum a čas plánovaného dodání nákladu** na odpovídající nákladu. Skladové místo na pevné záložce **Podrobnosti expedice** určuje skladové místo, na kterém je expedována objednávka transferu.
5.  Uvolněte do skladu v možnosti **Pracovní plocha plánování nákladu**.
6.  Vytvořte výrobní zakázku pro položku číslo **L0101** a nastavte stav na **Zahájeno** s množstvím 20.
7.  Vykázání jako dokončené z mobilního zařízení.
8.  Přejděte k portálu mobilního zařízení a vyberte položku nabídky **Ohlásit jako dokončené a odložit**.
9.  Vykažte číslo položky **L0101** jako dokončené z ručního zařízení. Všimněte si, že skladové místo je nyní **BAYDOOR 2**. Toto skladové místo lze nalézt z plánu událostí namísto směrnice skladového místa **Příjem transferu**.

### <a name="additional-information"></a>Doplňkové informace

-   Scénář cross dockingu je podporován pro dávku a sériové řízené zboží, přičemž jak dimenze dávky, tak dimenze sériového čísla jsou definovány nad a pod skladovým místem v hierarchii rezervací. 



