---
title: Skupiny výpočtů kusovníku
description: Tento článek obsahuje informace o skupinách výpočtu kusovníků, a o tom, jak je nastavit. Pro spuštění výpočtu kusovníku musíte buď nastavit skupiny kalkulace a přiřadit je k jednotlivým položkám, nebo nastavit výchozí skupinu výpočtu. Nastavení výpočtu ze skupiny výpočtu jsou použita jako výchozí hodnoty na stránce Kalkulace kusovníku v době výpočtu kusovníku.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5927b1c31cf15e2fb92c15d4abc06bfa0403e33d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266288"
---
# <a name="bom-calculations-groups"></a>Skupiny výpočtů kusovníku

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o skupinách výpočtu kusovníků, a o tom, jak je nastavit. Pro spuštění výpočtu kusovníku musíte buď nastavit skupiny kalkulace a přiřadit je k jednotlivým položkám, nebo nastavit výchozí skupinu výpočtu. Nastavení výpočtu ze skupiny výpočtu jsou použita jako výchozí hodnoty na stránce Kalkulace kusovníku v době výpočtu kusovníku. 

Uvedení výchozí skupiny výpočtu je požadováno na stránce **Parametry řízení zásob a skladu**, nebo je požadována skupina výpočtu konkrétních produktů na stránce **Podrobnosti o uvolněném produktu**. Systém nejprve hledá nastavení skupiny výpočtu na stránce **Podrobnosti o uvolněném produktu**. Pokud není skupina výpočtu nalezena, prohledá stránku **Parametry řízení zásob a skladu**. Pokud systém nenalezne skupinu výpočtu, uživatel obdrží během výpočtu chybovou zprávu. Skupina výpočtu obsahuje zásady pro model nákladové ceny, model prodejní ceny a kontrolní seznam upozornění. Nastavení výpočtu ze skupiny výpočtu jsou použita jako výchozí hodnoty na stránce **Kalkulace kusovníku** v době výpočtu kusovníku.

## <a name="purposes-of-bom-calculation-groups"></a>Účely skupin výpočtu kusovníku
Skupinu výpočtu kusovníku k položkám lze přiřadit z několika důvodů:

-   Nastavením pole **Model nákladových cen** určujete zdroj dat o příspěvcích nákladů nakupovaných komponent při výpočtu plánovaných nákladů na vyrobenou položku. Někteří výrobci chtějí počítat plánované náklady podle uzavřených smluv o nákupních cenách komponent nebo s využitím jiné základny, jako jsou záznamy o nákupních cenách v rámci nákladové verze.
-   Nastavením pole **Model prodejní ceny** určujete to, jak se použijí data o položce při výpočtu doporučené prodejní ceny. Můžete určit prodejní cenu položky nebo skupiny nákladů. Někteří výrobci požadují výpočet doporučené prodejní ceny vyrobených položek. Vypočtená prodejní cena můžete odrážet přístup „souhrnná cena“, který vychází ze záznamů o prodejní ceně pro komponentu. Případně může vypočtená prodejní cena odrážet přístup „náklady plus přirážka“, který vychází z nákladů komponent a použitého procenta zisku (přiřazeného k nákladové skupině položek).
-   Pomocí pole **Zastavit rozpad** určujete, že vyrobené zboží lze považovat za nakoupené zboží pro účely shrnutí nákladů při výpočtu kusovníku. Mezi typické příklady patří zakoupená položka, která je příležitostně vyráběnou položkou, nebo vyráběná položka, která je zakoupena. Daná položka je nejprve označena jako vyráběná položka s cílem definování údajů kusovníku a údajů o postupu nebo s cílem podpory výrobních zakázek pro danou položku. Nicméně příznak **Zastavit rozpad** zabraňuje výpočtům nákladů v používání kusovníku a postupu položky. Místo toho výpočet kusovníku používá zadané náklady pro zboží.

## <a name="calculation-groups"></a>Skupiny výpočtů
Můžete definovat skupiny výpočtů v části **Nastavení předem stanovených zásad pro náklady** v řízení nákladů. Skupiny výpočtů, které jsou přiřazeny k položkám, umožňují určit způsob, jak jsou nákladové komponenty nebo komponenty prodejní ceny (jak je uvedeno ve skupině výpočtu) získávány pro výpočet. Na stránce **Skupiny výpočtů** můžete definovat model nákladové ceny, alternativní model nákladové ceny, model prodejních cen a upozornění.

### <a name="cost-price-model"></a>Model nákladových cen

Existují čtyři možnosti pro pole **Model nákladové ceny**:

-   **Nákladová cena položky** – používá se nákladová cena z tabulky **Vydaný produkt** nebo se používá kombinace dimenzí položky jako nákladová cena.
-   **Nákupní cena položky** – používá se nákupní cena z pole **Nákladová cena** na kartě **Nákup** na stránce **Seznam uvolněných produktů**.
-   **Obchodní smlouvy** – můžete nakonfigurovat obchodní smlouvy pro určité kombinace položek a dodavatelů, nebo pro určitá pracoviště. Potom když zde vyberete možnost **Obchodní smlouvy**, použije se obchodní smlouva, kterou jste vytvořili pro nákupní cenu, společně se zbožím a pracovištěm.
-   **Cena zásob** – použije se aktuální hodnota zásob pro položku k výpočtu pořizovací ceny pro výpočet kusovníku. Pořizovací cena se vypočítá pouze tehdy, pokud je zaúčtované množství a fyzické množství větší než 0 (nula).

### <a name="alternative-cost-price"></a>Alternativní nákladová cena

Pole **Alternativní nákladová cena** má stejné možnosti jako pole **Model nákladové ceny**. Nicméně toto pole se používá pouze v případě, že cena nebyla nalezena v primárním modelu nákladové ceny.

### <a name="sales-price-model"></a>Model prodejních cen

Existují dvě možnosti pro výpočet pole **Prodejní ceny**:

-   **Nákladová skupina** – pokud je vybrána tato možnost, prodejní cena bude vypočtena na základě nákladové ceny a procenta z nastavení zisku ze skupiny nákladů.
-   **Prodejní cena zboží** – pokud je vybrána tato možnost, použije se prodejní cena na pevné záložce **Prodej** z tabulky Uvolněný produkt.

### <a name="stop-explosion"></a>Zastavit rozpad

Pole **Zastavit rozpad** slouží k určení toho, kdy se má vyrobené zboží považovat za nákupní položku. Obvyklé je ponechat pole **Zastavit rozpad** nezaškrtnuté. Zaškrtnutím tohoto políčka označíte, že s vyrobenou položkou se má pro účely výpočtu kusovníku zacházet jako s nakoupenou komponentou (místo jako s vyrobenou komponentou). V závislosti na pracovišti lze k výpočtu nákladů na položku i přesto použít kalkulace kusovníků. Rozpad plánované nákupní objednávky a výrobní zakázky je zastaven u kusovníku, jehož součásti jsou spojeny se skupinou výpočtu, u které je označeno pole **Zastavit rozpad**. Hlavní plánování generuje plánované objednávky přímo v kusovníku a ne u položek zahrnutých do kusovníku. V podstatě zaškrtnutím tohoto políčka určíte, že náklady nebudou přidány do kalkulace kusovníku pro položky, které mají tuto skupinu výpočtu.

### <a name="warnings"></a>Upozornění

Na pevné záložce **Upozornění** vyberte možnosti pro všechny zprávy s upozorněním, které mají uživatelé obdržet, pokud provedou výpočet kusovníku. 

Například, pokud označíte pole **Žádný kusovník**, uživatel obdrží upozornění, pokud není nalezena žádná aktivní verze kusovníku pro jednu z komponent nebo nadřízené zboží, u kterého je výpočet kusovníku spuštěn. Pokud označíte pole **Bez postupu**, uživatelé obdrží varování v případě, že není nalezena žádná aktivní verze postupu. Pokud používáte prostředky u vašich postupů a operací, můžete dát pokyn systému ke kontrole těchto prostředků. Poté pokud prostředek není nalezen na každém řádku v aktivním postupu, uživatel obdrží upozornění. 

Můžete také ověřit a zkontrolovat spotřebu. Spotřeba je množství v určitém postupu. Obvykle představuje množství času, které je vyžadováno k provedení určité operace pro výrobní proces. Můžete zkontrolovat, zda položka neobsahuje žádné nákladové ceny. Pokud neexistuje žádná aktivní nákladová cena pro položku, do výpočtu kusovníku se nepřidají žádné náklady. 

Můžete také zkontrolovat a ověřit věk nákladové ceny. Například zadáním hodnoty **60** označíte, že jednotková nákladová cena musí být znovu vyhodnocena po 60 dnech. Pokud je dosaženo tohoto omezení, systém vygeneruje upozornění. Například je v lednu tohoto roku zadána nákladová cena pro položku. Pokud je nyní srpen, což je více než 60 dnů poté, co byla zadána nákladová cena, uživatel obdrží upozornění při spuštění výpočtu kusovníku. Můžete zadat hodnotu v procentech do pole **Minimální příspěvková marže**. Tato hodnota označuje bod, do kterého není minimální příspěvková marže naplněna. Pokud příspěvková marže pro konkrétní součást není naplněna, uživatel obdrží upozornění. Toto pole proto pomáhá zaručit, že nejsou ohroženy náklady a další skladové náklady, které mohou být vyžadovány pro vaše položky.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Výchozí nastavení parametrů modulu Řízení zásob a skladu

Vzhledem k tomu, že jsou skupiny výpočtů požadovány pro spuštění výpočtů, musíte nastavit výchozí skupinu výpočtu v parametrech řízení zásob. Toto nastavení umožňuje společnostem využívat standardní nákladovou skupinu a nastavení zisku pro všechny položky. Má-li poté některá položka zvláštní požadavky na výpočet, uživatel může přiřadit jinou výpočetní skupinu k dané položce. Obvykle můžete nastavit skupiny výpočtů u položek součástí kusovníku namísto u položek kusovníku. Nicméně pokud se zobrazí upozornění, lze použít skupiny výpočtů. Skupina výpočtu, která je přiřazena ke zboží, přepíše výchozí hodnotu, která je nastavena v parametrech řízení zásob. 

Výchozí parametr můžete nastavit v části **Řízení nákladů** &gt; **Nastavení zásad skladového účetnictví** &gt; **Parametry** &gt; **Skladové účetnictví** &gt; **Skupina výpočtu**. Nastavením výchozí skupiny konfigurace můžete také nakonfigurovat podmínky pro upozornění, které se zobrazí uživatelům během procesu výpočtu kusovníku, pokud vybrané součásti mohou způsobit chyby ve výpočtu.

### <a name="view-warning-messages-on-the-complete-page"></a>Zobrazení upozornění na stránce Dokončeno

Výpočet kusovníku vygeneruje upozornění. Můžete zobrazit upozornění týkající se vybrané položky. Například v okně Prodej a marketing vytvořte novou prodejní objednávku pro položku D0001. Poté na řádku prodejní objednávky v nabídce **Aktualizovat řádek** klepnutím na tlačítko **Výpočet na základě kusovníku/vzorce** zobrazte podrobnosti o výpočtu a upozornění. Výsledky výpočtu kusovníku lze rovněž prohlížet na stránce **Dokončeno**. Pro upozornění: u vyráběných položek se používají pouze dvě podmínky výstrah, zatímco u všech ostatních položek se používají čtyři podmínky výstrah:
-   Identifikovat, když vyráběná položka nemá aktivní kusovník.
-   Identifikovat, když vyráběná položka nemá aktivní technologický postup.
-   Identifikovat, když položka na řádku kusovníku má uvedené nulové množství.
-   Identifikovat, když položka na řádku kusovníku má uvedené nulové náklady nebo když nemá záznam o nákladech.
-   Identifikovat, když položka na řádku kusovníku má zastaralé náklady. Upozornění vychází z porovnání data výpočtu s určitým počtem dnů, který vyjadřuje maximální stáří ceny.
-   Identifikovat, když položka na řádku kusovníku má menší procento ziskovosti, než jaké požadujete.

Můžete definovat několik skupin výpočtů kusovníku v závislosti na požadavcích na variaci u varovných zpráv. Jedna skupina výpočtu kusovníku může být například dostačující pro podmínky výstrah týkající se aktivního kusovníku, nulového množství a nulových nákladů komponenty. Po zahájení výpočtu kusovníku můžete přepsat použité podmínky výstrah, které jsou přidružené ke skupině výpočtu kusovníku. Můžete také přidat nebo odebrat podmínky upozornění. Když například aktuální situace nezahrnuje data technologického postupu, můžete odebrat použitou podmínku výstrah, která se týká aktivního postupu. **Poznámka:** čas a docházka zahrnuje stránku **Skupiny výpočtů**, ale tato stránka nemá žádný vztah ke skupinám výpočtu kusovníku. V části Čas a docházka lze pracovníky přiřadit ke skupinám výpočtů, které odrážejí sdružení pracovníků, kteří jsou přidruženy ke stejnému nadřízenému nebo vedoucímu. Výpočet registrací pracovníků může provést automaticky nebo ručně jejich nadřízený nebo vedoucí.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]