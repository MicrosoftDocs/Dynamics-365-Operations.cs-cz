---
title: Potvrdit a převést
description: V tomto tématu se vysvětluje, jak používat funkci Potvrdit a převést, která uživatelům umožňuje expedovat náklady ze skladu dříve, než je dokončena veškerá práce s těmito náklady spojená.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6104e457a62f340951c187d0f2dbe48b0dffdf7f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423580"
---
# <a name="confirm-and-transfer"></a>Potvrdit a převést

[!include [banner](../includes/banner.md)]

Funkce *Potvrdit a převést* umožňuje uživatelům expedovat náklady ze skladu dříve, než je dokončena veškerá práce s těmito náklady spojená. Když je přijata zásilka, která obsahuje řádky nakládky, které ještě nebyly kompletně vydány, je potvrzující uživatel vyzván, aby zbývající množství rozdělil a vytvořil tak nový náklad nebo aby neúplná množství zrušil.

Systémy, které jsou nastaveny tak, aby umožňovaly dělení nákladu, podporují scénáře, kdy je třeba z důvodu nových nebo měnících se okolností upravit plánované a částečné náklady.

Klient zahrnuje logiku, jež umožňuje uzavřít částečné náklady a potvrdit je jako expedované. Všechny zbývající zásilky a řádky nakládky (včetně úplných nebo částečných řádkových množství) se poté převedou do nově vytvořeného nákladu a zásilky, pokud je tento převod požadován a nastavení to umožňuje. Nové zásilky a náklady se vytvářejí automaticky na základě počátečních kritérií vytváření zásilek a nákladů. Jejich hlavní atributy zůstávají nezměněny. Existuje také možnost zbývající množství automaticky zrušit, pokud ještě nebyl vytvořen pracovní příkaz a uživatel považuje zrušení za nutné.

Tato funkce podporuje scénáře, kdy se celý náklad nevejde na jeden kamion nebo kde by část nákladu měla opustit sklad dříve, než bude zbytek nákladu připraven k dodávce. V těchto scénářích lze zbývající produkty převést do nového nákladu, tedy do nového kamionu. Vzhledem k tomu, že tuto funkci lze použít u nákladů, jež by jinak vyžadovaly celovozovou přepravu, nabízí zvláštní flexibilitu, a proto umožňuje manažerům dopravy řešit nestandardní nebo nepředvídané scénáře.

Když je náklad rozdělen, funkce *Potvrdit a převést* provede následující akce:

- Dle potřeby se vytvoří nové náklady a dodávky. Každý náklad nebo každá dodávka bude mít maximální možné množství atributů shodných s původním nákladem nebo s původní dodávkou. Výjimkou je stav nákladu, který bude přepočítán na základě stavu práce.
- Uživatel je informován, že byl vytvořen nový náklad. Uživatel je též informován o ID nového nákladu.
- Řádky nákladu, záhlaví práce a řádky práce, jež byly děleny, se aktualizují s využitím údajů o novém nákladu a dodávce.
- Pokud se dělí celá dodávka, je dodávka zachována a aktualizují se pouze reference na náklad. Pokud musí být dodávka dělena, vytvoří se nová dodávka.

Když jsou zbývající množství zrušena, budou z nákladu odstraněna všechna množství v nákladových řádcích, jež nebyla vydána a k nimž není přidružena nezrušená práce. Pokud probíhá nějaká práce, uživatel může rozdělit pouze náklad. Zbývající množství nelze zrušit.

Můžete rozdělit pouze náklady, jež splňují všechna následující kritéria:

- V jednom nebo více řádcích nákladu jsou vydaná množství.
- Stav nákladu je nižší než naložen.
- Neexistují data řádku nákladu. (Tato data se vytvářejí konsolidací registračních značek na přechodném skladovém místě, funkce *Potvrdit a převést* konsolidaci registračních značek nepodporuje.)
- Žádné zásoby aktuálně nečekají na balení v balicím místě. (Funkce *Potvrdit a převést* nepodporuje zásoby, které byly vydány do balicí stanice, ale ještě nebyl zabaleny.)

> [!NOTE]
> Tato funkce se liší od funkce nákladu přepravy, kterou je vhodné použít ve skladech, které nikdy nemohou plánovat a vytvářet náklady před výdejem ale místo toho nakládají do dostupného přepravního prostoru po dokončení výdeje.
>
> Funkci *Potvrdit a převést* použijte v situacích, kdy se náklady obvykle plánují a vytvářejí, ale někdy se vyskytují případy, kdy se náklad do dostupné přepravy nevejde (například do kamionu).

## <a name="turn-on-confirm-and-transfer"></a>Zapnutí funkce Potvrdit a převést

Než můžete použít funkci *Potvrdit a převést*, musíte ji v systému zapnout. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Potvrdit a převést*

## <a name="set-up-confirm-and-transfer"></a>Nastavení funkce Potvrdit a převést

Chcete-li použít funkci *Potvrdit a převést*, musíte tuto funkci zapnout v každé relevantní šabloně nákladu. Navíc, v závislosti na vašich požadavcích, můžete chtít připravit šablony práce, které tuto funkci podporují. Pokud chcete využít scénář uvedený v tomto tématu jako příklad, nastavte systém podle popisu v této části. (Tento scénář je založen na ukázkových datech **USMF**.)

### <a name="prepare-your-load-templates"></a>Příprava šablon nákladů

1. Přejděte do **Řízení skladu \> Nastavení \> Náklad \> Šablony nákladů**.
1. V podokně Akce vyberte možnost **Upravit**, tím přepnete stránku režimu úprav.
1. Zaškrtněte políčko **Povolit rozdělení nákladu během potvrzení dodávky** pro každou existující šablonu, ve které chcete funkci zapnout. Případně můžete také kliknout na **Nový** a vytvořit novou šablonu a tu si nakonfigurovat podle potřeb. Každý náklad, který pomocí této šablony vytvoříte, pak tuto funkci zdědí. (Pokud pracujete s ukázkovými daty **USMF**, zapněte funkci pro šablonu nákladu **20' kontejner**.)

### <a name="prepare-your-work-templates"></a>Příprava šablon práce

Toto nastavení není nezbytné ve všech situacích. Zde uvedený příklad zajišťuje, že práci lze členit podle dodávek. Díky tomu podporuje ukázkový scénář uvedený dále v tomto tématu. Tohoto výsledku lze dosáhnout i jinými způsoby.

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. V mřížce v horní části stránky vyberte existující šablonu práce, v níž chcete nastavit funkci *Potvrdit a převést*. (Pokud pracujete s ukázkovými daty **USMF**, vyberte šablonu práce **51 Výdej do přípravy**.) Další možností je vytvořit novou šablonu práce.
1. V podokně Akce zvolte možnost **Upravit dotaz** a otevřete dialogové okno **Prodej**.
1. V dialogovém okně **Prodej** klikněte na kartu **Třídění** a tlačítkem **Přidat** přidejte řádek mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *Dočasné pracovní transakce*
    - **Odvozená tabulka:** *Dočasné pracovní transakce*
    - **Pole:** *ID dodávky*
    - **Směr hledání:** *Vzestupně*

1. Volbou **OK** uložte nastavení a zavřete dialogové okno **Prodej**.
1. Pokud obdržíte zprávu, že seskupení bude resetováno, pokračujte kliknutím na **Ano**.
1. V mřížce v horní části stránky **Šablony práce** vyberte šablonu, kterou jste právě upravili. Poté v podokně Akce vyberte možnost **Zalomení pracovních hlaviček**.
1. V podokně Akce vyberte možnost **Upravit**, tím přepnete stránku režimu úprav.
1. V mřížce nastavte následující hodnoty:

    - **Název tabulky:** *Dočasné pracovní transakce*
    - **Název pole:** *ID dodávky*
    - **Seskupit podle tohoto pole:** Toto políčko zaškrtněte.

1. V podokně akcí vyberte **Uložit**.
1. Zavřete stránku.

## <a name="scenario"></a>Scénář

Tento scénář zachycuje příklad, kdy není ještě proces výdeje dokončen, ale položky, které již byly vydány, musí být naloženy do kamionu a expedovány. Uživatel proto může rozdělit řádky s nevydaným nákladem do nového nákladu. Následně se provede automatická aktualizace všech datových vztahů.

> [!NOTE]
> Konkrétní hodnoty popsané v tomto scénáři vycházejí z ukázkových dat **USMF**. Doporučujeme tato ukázková data používat v rámci ukázek nebo výuky práce s touto funkcí. Pokud nepoužíváte ukázková data **USMF**, nahraďte ukázkové hodnoty svými hodnotami, jak je to třeba.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>Krok 1: Vytvoření nákladu, který má více řádků nákladu

K použití této funkce musíte mít náklad, které obsahuje více řádků nákladu. Je třeba též zajistit, aby skladová místa pro výdej měla dostatečné množství zásob pro všechny položky prodejních objednávek, jež budete vytvářet. Zkontrolujte nastavení směrnice skladového místa (**Řízení skladu \> Nastavení \> Směrnice skladového místa**) a poznamenejte si, která výdejová skladová místa se používají pro výdej prodejní objednávky. Pokud musíte upravit zásoby, vytvořte ruční pohyby, použijte doplnění nebo využijte jakýkoli jiný tok, jak je třeba.

Chcete-li vytvořit kvalifikovaný náklad, nejprve následujícím postupem vytvořte tři prodejní objednávky.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně Akce zvolte možnost **Nová** a otevře se dialogové okno **Vytvoření prodejní objednávky**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte (minimálně) následující hodnoty:

    - Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-004* (*Cave Wholesales*).
    - Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *51*.

1. Stisknutím **OK** vytvoříte prodejní objednávku a zavřete dialogové okno **Vytvoření nákupní objednávky**.
1. Otevře se nová prodejní objednávka. V mřížce **Řádky prodejní objednávky** přidejte řádek s následujícími hodnotami:

    - **Číslo položky:** *M9200*
    - **Množství:** *40*
    - **Jednotka:** *EA*

1. V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. V podokně Akce vyberte možnost **Rezervovat šarži**, otevře se stránka **Rezervace**.
1. Rezervujte si zásoby z řádku prodejní objednávky, stránku **Rezervace** poté zavřete.
1. Opakováním kroků 1 až 4 přidejte druhou prodejní objednávku pro stejného zákazníka a sklad.
1. Přidejte dva řádky prodejní objednávky s následujícími hodnotami. Po přidání každého řádku rezervujte zásoby způsobem popsaným v krocích 6 až 8.

    - **Řádek 1:** Nastavte v poli **Číslo položky** hodnotu *M9200*, v poli **Množství** hodnotu *30* a v poli **Jednotka** hodnotu *ks*.
    - **Řádek 2:** Nastavte v poli **Číslo položky** hodnotu *M9201*, v poli **Množství** hodnotu *20* a v poli **Jednotka** hodnotu *ks*.

1. Opakováním kroků 1 až 4 přidejte třetí prodejní objednávku pro stejného zákazníka a sklad.
1. Přidejte dva řádky prodejní objednávky s následujícími hodnotami. Po přidání každého řádku rezervujte zásoby způsobem popsaným v krocích 6 až 8.

    - **Řádek 1:** Nastavte v poli **Číslo položky** hodnotu *M9201*, v poli **Množství** hodnotu *20* a v poli **Jednotka** hodnotu *ks*.
    - **Řádek 2:** Nastavte v poli **Číslo položky** hodnotu *M9202*, v poli **Množství** hodnotu *60* a v poli **Jednotka** hodnotu *ks*.

#### <a name="load-planning-workbench"></a>Pracovní plocha plánování vytížení

Nástroj pro plánování vytížení použije ID šablony nákladu k vytvoření dodávek a uvolnění řádků prodejní objednávky do skladu.

1. Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.
1. V poli **Sklad** zvolte *51*.

    Nyní vytvoříte náklad pro právě vytvořené prodejní objednávky.

1. V mřížce na kartě **Řádky prodejů** vyberte řádky prodejů pro nové prodejní objednávky.
1. V podokně Akce na kartě **Nabídka a poptávka** vyberte ve skupině **Přidat** možnost **Do nového vytížení**.
1. V dialogovém okně **Přiřazení šablony nákladu** nastavte v poli **ID šablony nákladu** hodnotu *20' kontejner*.
1. Vyberte **OK**.
1. V části **Náklady** na stránce **Nástroj pro plánování vytížení** vyhledejte v mřížce nově vytvořené ID nákladu pro sklad *51*. Posuňte se doprava, až uvidíte sloupec **Povolit rozdělení nákladu během potvrzení dodávky**. Je třeba zaškrtnout políčko by pro příslušný náklad.
1. Vyberte náklad.
1. V nabídce **Uvolnění** nad mřížkou vyberte možnost **Uvolnění do skladu**, aby se vytvořila práce.
1. V dialogovém okně **Uvolnit náklad do skladu** ověřte, že se na záložce s náhledem **Záznamy k zahrnutí** zobrazuje ID vašeho nákladu.
1. Vyberte **OK**.

    Zatímco systém vytváří dodávky a práce, může se zobrazovat zpráva „Provádí se operace“.

1. V části **Náklady** na stránce **Nástroj pro plánování vytížení** by nyní měl mít náklad stav *Zařazeno do vlny*. Vyberte náklad a poté v nabídce nad mřížkou **Související informace** vyberte **Podrobnosti vlny**. Zobrazí se ID vytvořených dodávek. Po skončení stránku **Vlny** zavřete.
1. V části **Náklady** na stránce **Nástroj pro plánování vytížení** vyberte náklad a poté v nabídce **Související informace** nad mřížkou vyberte možnost **Podrobnosti práce**. Zobrazí se práce vytvořená pro prodejní objednávky.
1. Poznamenejte si ID vytvořených prací. Možná budete muset posunout zobrazení doprava, aby se zobrazilo číslo prodejní objednávky a ID dodávky přiřazených k ID práce.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>Krok 2: Nastavení toku spouštění pro mobilní zařízení

Úlohy mobilních zařízení budou vyžadovat zadání údajů uživatelem, například ID práce nebo ID registrační značky. V terénu mají tyto informace obvykle podobu čárových kódů, které se nacházejí v dokumentaci, na obalech nebo na regálech. Chcete-li provést v rámci scénářů kroky pro mobilní zařízení, ujistěte se, že máte určená ID prací pro příslušné transakce a ID registračních značek pro položku a skladové místo v transakcích.

1. Přihlaste se k mobilnímu zařízení pomocí ID uživatele a hesla pro sklad *51*.
1. Vyberte **Odchozí**.
1. Vyberte **Prodejní výdej**.
1. Máte možnost zadat ID práce nebo ID registrační značky. Zadejte ID práce pro první prodejní objednávku, poté stiskněte **Vstup**.
1. V poli **Loc** zadejte skladové místo, které se zobrazí. Výdejové skladové místo se tak potvrdí. Poté stiskněte **Vstup**.
1. V poli **LP** zadejte ID registrační značky. ID registrační značky musí odpovídat položce, skladu a skladovému místu položky, která je z vybraného skladového místa vydávána. Po dokončení stiskněte **Vstup**.
1. V poli **Položka** zadejte číslo položky, výběr položky potvrďte a poté stiskněte **Vstup**.
1. V poli **Množ.** zadejte množství, jež se vydává, a poté stiskněte **Vstup**.
1. V poli **Cílová RZ** zadejte ID cílové registrační značky. Cílové registrační značky jsou definovány uživatelem. Nezapomeňte zadat takové ID registrační značky, jaké si snadno zapamatujete. Doporučujeme použít jako formát aktuální datum plus dvě číslice (RRMMDD\#\#), například *19112301*. Po dokončení stiskněte **Vstup**.
1. Zkontrolujte zobrazené informace. Tato informace jsou *výdejové* informace, jež se nyní stanou *zaskladňovacími* daty pro transakci zaskladnění. Po dokončení stiskněte **Vstup**.

    - Zobrazí se zpráva **Práce dokončena**.

1. Opakujte kroky 4 až 10 pro ID práce druhé prodejní objednávky.

V dalším kroku je třeba naložit dvě vybrané registrační značky na kamion.

1. Přihlaste se k mobilnímu zařízení pomocí ID uživatele a hesla pro sklad *51*.
1. Vyberte **Odchozí**.
1. Vyberte **Nakládání prodeje**.
1. Zadejte uživatelem definované ID cílové registrační značky, jak jste vytvořili pro první ID práce v předchozí proceduře. Poté stiskněte **Vstup**, tím se cílová registrační značka vloží do **PŘÍPRAVNÉHO** skladovacího místa.
1. Zadejte znovu ID cílové registrační značky a poté stiskněte **Vstup**. Registrační značka se vloží do skladového místa **PORTÁL**.
1. Zopakujte kroky 4 až 5 pro ID cílové registrační značky vytvořené pro druhé ID práce.

Obě ID práce budou nyní uzavřena (naložena).

### <a name="step-3-confirm-the-outbound-shipment"></a>Krok 3: Potvrzení odchozí dodávky

V tomto kroku potvrdíte dvě prodejní objednávky a práce, které byly dokončeny pro naložení dodávky vydaných položek nákladu a vytvoření nového nákladu pro nevydané položky. Potvrzení odchozí dodávky musí být provedeno na stránce **Podrobnosti nákladu**.

1. Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.
1. V mřížce v části **Náklady** vyberte řádek vytvořeného ID nákladu.
1. Kliknutím na odkaz ID nákladu otevřete stránku **Podrobnosti nákladu**.
1. Na stránce **Podrobnosti nákladu** v podokně Akce vyberte na kartě **Expedovat a přijmout** ve skupině **Potvrdit** položku **Odchozí dodávka**. Tím inicializujete potvrzení.
1. V dialogovém okně **Potvrdit dodávku** vyberte v poli **Metoda dělení nákladu během potvrzení dodávky** možnost *Rozdělit množství do nového nákladu*.
1. Vyberte **OK**.

    Může se zobrazit zpráva „Provádí se operace“.

    Zobrazí se zprávy, které uvádějí, že dodávka vztahující se k nákladu byla potvrzena a že z rozděleného množství byl vytvořen nový náklad.

Aktualizujte stránku **Nástroj pro plánování vytížení**. Zobrazí se na ní i nově vytvořený náklad.

O aktualizaci transakčních vztahů se můžete ujistit také takto:

- Zbývající (nezpracované) dodávky a řádky dodávek se aktualizují (nové ID nákladu).
- Prodejní objednávka je propojena s novým ID nákladu.
- Původní náklad nezahrnuje zbývající řádky nákladu.
- Zbývající práce byla aktualizována s použitím nového ID nákladu.
- Vlna zůstává beze změny.
- Stav nového nákladu je správně aktualizován. (Pokud je stav práce _V procesu_, měl by být ve stavu _V procesu_ také náklad.)

## <a name="notes-and-tips"></a>Poznámky a tipy

- Také můžete zapnout parametr **Povolit rozdělení nákladu během potvrzení dodávky**, chcete-li vytvářet náklad při vypnutém parametru **Šablona nákladu**, ale před zahájením procesu nakládání. Přejděte na požadovaný náklad, poté v zobrazení záhlaví parametr zapněte.
- Možnost **Rozdělit množství do nového nákladu** funguje také tehdy, když jsou některá ze zbývajících záhlaví ve stavu *V procesu*. Funkci proto můžete používat, i když pracovníci již provádějí příkazy k výdeji.
- Pokud vyberete možnost **Stornovat nedodané množství**, zatímco ještě existuje práce ve stavu *Otevřená* nebo *Probíhající*, zobrazí se následující chybová zpráva: „Nelze stornovat zbývající množství pro naložení. Existuje práce pro nakládání.“
- Pokud vyberete možnost **Stornovat nedodané množství**, když již nezbývá žádná práce, ale existují neexpedované řádky nákladu, zobrazí se následující chybová zpráva: „Zásilku nelze načíst, protože množství u položky překračuje procento definované pro dodávku.“ Chcete-li se této chybě vyhnout, můžete nastavit procentuální hodnotu **V dodávce** na nerealizovaném řádku nákladu na 100 procent. Nerealizované řádky nebudou přesunuty do nového nákladu, ale aktuální náklad bude potvrzen jako „v dodávce“. V takovém případě nebudete moci původní objednávku znovu uvolnit. Proto bude třeba věc vyřešit jiným postupem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]