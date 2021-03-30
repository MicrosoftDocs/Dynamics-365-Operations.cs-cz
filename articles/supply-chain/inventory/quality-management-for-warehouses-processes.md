---
title: Správa kvality pro procesy skladu
description: V tématu jsou informace týkající se procesu řízení kvality pro funkci procesů skladu. Tato funkce rozšiřuje možnosti správy kvality a umožňuje uživatelům integrovat ovládací prvky vzorkování položek do skladového procesu příjmu pomocí pokročilé správy skladu.
author: Henrikan
manager: tfehr
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: e2bf8e340115b03577779d50ba03be8341535d87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209652"
---
# <a name="quality-management-for-warehouse-processes"></a>Správa kvality pro procesy skladu

Funkce _Správa kvality pro procesy skladu_ umožňuje integrovat ovládací prvky vzorkování položek do skladového procesu příjmu pomocí pokročilé správy skladu. Skladová práce může být automaticky generována pro přesunutí zásob do skladového místa řízení kvality, na základě procentuálního nebo fixního množství nebo na základě každé *n-té* registrační značky. Po dokončení objednávky kvality lze automaticky vygenerovat práci, aby bylo možné přesunout zásoby do dalšího místa v procesu v závislosti na výsledcích kvality.

Funkce _Správa kvality pro procesy skladu_ rozšiřuje možnosti základní správy kvality. Poskytuje možnost vytvořit objednávky kvality pro zásoby, které jsou odesílány do skladového místa řízení kvality, ačkoliv objednávky kvality nejsou vždy požadovány. Proto umožňuje lehký proces řízení kvality, který je založen na práci ve skladu.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Zapněte funkci Správa kvality pro procesy skladu

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Správa kvality pro procesy skladu*

## <a name="key-benefits"></a>Klíčové výhody

Funkce _Správa kvality pro procesy skladu_ automaticky generuje práci v rámci procesu příjmu, aby bylo možné přesunout množství zásob, které je požadováno pro řízení kvality, do umístění kontroly kvality. Pokud přijaté množství překračuje množství vyžadované pro řízení kvality (podle nastavení vzorkování zboží), přebytek množství bude přesunuto do vstupního skladového místa, které je definováno v nastavení směrnice o skladovém místě. Po ověření objednávky kvality je automaticky vygenerována práce s cílem přesunout množství objednávky kvality do nového vstupního nebo návratového místa na základě výsledků ověření a nastavení směrnice skladového místa. Automatické generování práce, které má pouze množství, které musí být přesunuto do a ze řízení kvality, poskytuje integrovaný proces práce.

> [!NOTE]
> Je-li funkce _Správa kvality pro procesy skladu_ zapnuta, můžete přesto využít výhod ručního zpracování. V ručním procesu se při vytvoření skladové práce pomocí šablony použije pracovní postup skladu, který vytvoří skladové množství pro přesun zásob z místa řízení kvality do nového místa. Můžete také přesto nastavit směrnici pro příchozí skladové místo, která zcela přesune zásoby z přijímacího místa do místa řízení kvality, aniž by bylo nutné zvážit nastavení vzorkování zboží.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Funkce Správa kvality a Správa kvality pro procesy skladu

Je-li _Správa kvality pro procesy skladu_ zapnuta, změní se nastavení klíčových subjektů správy skladu a správy kvality. Na následujícím obrázku je uveden přehled entit, které umožňují objednávky kvality pro procesy skladu. Text v závorkách označuje doporučené akce při použití správy kvality před zapnutím fukce _Správa kvality pro procesy skladu_.

![Entity správy kvality](media/quality-management-entity-diagram.png "Entity správy kvality")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Aktivátory: typy pracovní objednávky pro vzorkování položek kvality a pořadí kvality

Funkce _Správa kvality pro procesy skladu_ zavádí dva typy pracovních příkazů, které umožňují proces vytváření práce:

- **Vzorkování položky kvality** – tento typ pracovní objednávky slouží k vytvoření práce, která přesune registrované zásoby do řízení kvality.
- **Objednávka kvality** – tento typ pracovního příkazu se používá k vytvoření práce, která přesouvá zásoby z řízení kvality do nového umístění na základě nastavení směrnice o skladovém místě.

### <a name="work-classes-location-directives-and-work-templates"></a>Pracovní třídy, směrnice umístění a šablony práce

Typy pracovní objednávky _Vzorkování položky kvality_ a _Objednávka kvality_ jsou spotřebovány podle směrnic o umístění, třídách práce a šablon práce.

Před tím, než může být automaticky vygenerována práce na skladě pro přesunutí zásob do řízení kvality, je nutné provést následující kroky a nastavit systém.

1. Vytvoření samostatných tříd práce pro typy pracovní objednávky _Vzorkování položky kvality_ a _Objednávka kvality_. Tímto způsobem zajistíte, že bude možné automaticky generovat odpovídající práci na základě dvou typů pracovních příkazů a že tato práce může být spuštěna pomocí aplikace skladu.
1. Nastavte pracovní šablonu pro každý typ pracovního příkazu:

    - Chcete-li automaticky přesunout registrované zásoby do umístění kontroly kvality, nastavte šablonu práce, která používá typ pracovního příkazu _Vzorkování položky kvality_.
    - Chcete-li přesunout registrované zásoby z umístění kontroly kvality po dokončení kontroly kvality, nastavte šablonu práce, která používá typ pracovního příkazu _Objednávka kvality_.

1. Pro každý typ pracovního příkazu nastavte směrnice skladových míst, které používají správná pracoviště pro řízení kvality, do kterých mají být zásoby přesunuty. Po dokončení řízení kvality směrnice skladového místa pro typ pracovního příkazu _Objednávka kvality_ zajistí, aby bylo vybráno nové cílové skladové místo, aby bylo možné sklad přesunout z umístění kontroly kvality.
1. Nastavte příslušné položky nabídky mobilního zařízení tak, aby podporovaly pohyb přijatých zásob do umístění pro řízení kvality, a pohyb zásob, které procházejí nebo selžou řízení kvality z umístění řízení kvality do nového umístění.

Podrobný příklad, který ukazuje, jak dokončit toto nastavení, naleznete ve [ukázkovém scénáři](#example-scenario) na konci tohoto tématu.

## <a name="enable-a-warehouse-for-quality-management"></a>Povolte sklad pro řízení kvality

Dříve, než bude možné použít funkci _Správa kvality pro procesy skladu_ pro určitý sklad, je třeba tuto funkci pro daný sklad zpřístupnit pomocí následujících kroků.

1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
1. Vyberte sklad pro povolení řízení kvality.
1. Na pevné záložce **Sklad** nastavte možnost **Povolit objednávku kvality pro skladové procesy** na _Ano_. (Tato možnost může být nastavena na hodnotu _Ano_ pouze u skladů, které používají procesy správy skladu.)

Pokud je možnost **Povolit objednávku kvality pro skladové procesy** nastavena na hodnotu _Ano_, nastavení přiřazení kvality určuje, zda je pro vybraný sklad skutečně použita funkce _Správa kvality pro procesy skladu_. Kdykoli můžete změnit nastavení možnosti na _Ne_. V takovém případě se funkce nebude nadále používat pro sklad bez ohledu na nastavení přiřazení kvality.

## <a name="quality-control"></a>Řízení kvality

Funkce _Správa kvality pro skladové procesy_ řídí několik klčových nastavení pro přidružení kvality a vzorkování položek.

### <a name="quality-associations"></a>Přiřazení kvality

Každý [záznam o přidružení kvality](enable-quality-management.md) určuje sadu testů, přijatelnou úroveň kvality (AQL) a plán vzorkování, které platí pro vygenerované objednávky kvality. Chcete-li nastavit záznam o přidružení kvality, postupujte podle následujících pokynů.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Přiřazení kvality**.
1. Vytvořte nebo vyberte položku Přiřazení kvality pro položku nebo skupinu, s níž pracujete, nebo pro všechny položky.
1. Na pevné záložce **Podmínky** nastavte pole **Použitelný typ skladu** na jednu z následujících hodnot:

    - **Pouze Správa kvality pro procesy skladu** – aktivujte funkci _Správa kvality pro procesy skladu_. Tuto hodnotu můžete vybrat pouze v případě, že typ odkazu je *Nákup* nebo *Výroba*.
    - **Všechny** – deaktivujte funkci _Správa kvality pro procesy skladu_. Tuto hodnotu vyberte pro všechny typy odkazů s výjimkou *Nákupu* a *Výroby*.

> [!NOTE]
> Funkce _Správa kvality pro procesy skladu_ se uplatní pouze v případě, že položka na řádku zdrojového dokumentu používá pokročilé procesy správy skladu a pokud je možnost **Povolit objednávku kvality pro skladové procesy** nastavena na _Ano_ pro sklad v řádku zdrojového dokument.

Jak je každá položka registrována (nebo hlášena jako dokončená), systém určí, která přiřazení kvality použije.

Je-li funkce _Správa kvality pro procesy skladu_ zapnuta, bude příslušný typ skladu logicky vložen do čtvrté skupiny vyhledávání hierarchie vyhledávání přiřazení kvality. V následující tabulce jsou uvedeny logické reprezentace hierarchie vyhledávání.

| Hledat skupinu | popis |
|---|---|
| Skupina 1 | U každého přiřazení kvality zkontrolujte **Typ odkazu**, **Typ události** a hodnoty **Párování spuštění** pro danou položku. Pokud existuje párování s řádkem zdrojového dokumentu, přesuňte se do skupiny 2. |
| Skupina 2 | U každého přiřazení kvality zkontrolujte hodnotu **Kódu položky** (_tabulka_, _skupina_ nebo _vše_) pro danou položku. _Tabulka_ je konkrétnější než _Skupina_ a _Skupina_ je konkrétnější než _Vše_. Pokud existuje párování pro _Tabulku_ (specifickou položku), přesuňte se do skupiny 3. Pokud pro _Tabulku_ neexistují žádné párování, vyhledejte párování pro _Skupinu_. Není-li pro _skupinu_ nalezeno žádné párování, platí možnost _Vše_. Pokud existuje párování, přesuňte se do skupiny 3. |
| Skupina 3 | U každého přiřazení kvality zkontrolujte **Kód účtu** a hodnoty **Zdrojového kódu** pro danou položku. Použitá logika se podobá logice použité pro hodnotu **kódu položky**. |
| Skupina 4 | U každého přiřazení kvality zkontrolujte pro danou položku hodnotu **Použitelný typ skladu** (_Pouze správa kvality pro procesy skladu_ nebo _vše_). Je-li možnost **Povolit objednávku kvality pro skladové procesy** nastavena na _Ano_ pro sklad ve zdrojovém dokumentu a položka na řádku zdrojového dokumentu je nastavena na _Použít procesy řízení skladu_, přidružení, kde existuje párování pro _Pouze Správa kvality pro procesy skladu_ a přidružení, kde existuje párování pro _Vše_, platí souběžně, pokud existují. Pokud je možnost **Povolit objednávku kvality pro skladové procesy** nastavena na _Ne_ pro sklad ve zdrojovém dokumentu a položka na řádku zdrojového dokumentu je nastavena na _Použít procesy řízení skladu_, použije se pouze správa kvality. |

Definovali jste například sklad, ve kterém je možnost **Povolit objednávku kvality pro skladové procesy** nastavena na hodnotu _Ano_, a máte dvě přiřazení kvality, která jsou definována pro typ odkazu *Nákup*: jedna pro všechny položky a jedna pro typ události *Registrace*. Jediný rozdíl mezi dvěma přiřazeními kvality je hodnota **Použitelný typ skladu**: je nastavena na _Vše_ pro jedno přidružení kvality a _Pouze správa kvality pro procesy skladu_ pro ostatní. V takovém případě jsou obě přidružení kvality stejná jako specifická a obě se použijí.

Hodnota pole **Testovací skupina** pro přiřazení kvality je také koeficientem. Toto pole definuje postup testování, který je nutné použít. Hodnota **Testovací skupina** je stejná pro obě přiřazení, bude vytvořena pouze jedna objednávka kvality pro přiřazení kvality, kde hodnota **Použitelný typ skladu** je _Pouze správa kvality pro procesy skladu_. Pokud hodnota **Testovací skupina** není pro obě přidružení shodná, budou vytvořeny dvě objednávky kvality. První objednávka kvality bude vytvořena pro přidružení kvality, kde hodnta **Použitelný typ skladu** je _Pouze správa kvality pro procesy skladu_. Druhá objednávka kvality bude vytvořena pro přidružení kvality, kde hodnta **Použitelný typ skladu** je _Vše_.

> [!NOTE]
> Hodnota _Pouze správa kvality pro procesy skladu_ je považována za konkrétnější než _Vše_, pokud kritéria pro přiřazení kvality pro skupiny 1 a 2 jsou shodná a pokud je testovací skupina stejná. Dvě objednávky kvality budou vytvořeny pouze v případě, že se testovací skupiny liší.

#### <a name="reference-types"></a>Typy odkazů

Pokud je hodnota **Referenční typ** nastavena na _Nákup_ a hodnota **Použitelný typ skladu** je _Pouze správa kvality pro procesy skladu_, pole **Typ události** na pevné záložce **Proces** musí být nastavena na _Registraci_. _Registrace_ je jediným podporovaným typem události pro typ odkazu _Nákup_, když používáte funkci _Správa kvality pro procesy skladu_.

#### <a name="quality-processing-policy"></a>Zásada zpracování kvality

Funkce _Správa kvality pro procesy skladu_ umožňuje vytvoření práce na základě pouze vzorkování položky. Proto umožňuje lehký proces. Sklad, v němž je práce vytvořena, závisí na vzorkování položky, které je spojeno s přiřazením kvality. Když se použije lehký proces, poté, co pracovník zaznamená množství do umístění kontroly kvality, může oddělení kvality ručně vytvořit objednávku kvality, pokud je vyžadována objednávka kvality.

Pole **Zásady zpracování kvality** na pevné záložce **Proces objednávky kvality** určuje, zda je při vytvoření práce pro přesunutí položky do umístění řízení kvality vytvořena také objednávka kvality. Toto pole lze nastavit pro _Vytvoření objednávky kvality_ nebo _Vytvořit pouze práci_. Výchozí hodnota je _Vytvořit objednávku kvality_.

> [!NOTE]
> Bez ohledu na to, zda vytváříte objednávky kvality ručně nebo automaticky, systém automaticky vygeneruje práci pro přesun položek z místa řízení kvality, když je objednávka kvality označena jako ověřená.

Vytvoření pracovní objednávky kvality nesouvisí s nastavením přiřazení kvality. Pokud existuje pracovní šablona, která má hodnotu **Typ pracovního příkazu** *Objednávka kvality* a pokud jsou pro tuto šablonu práce splněna kritéria dotazu, bude při ověření objednávky kvality spuštěna tvorba objednávky kvality.

#### <a name="referenced-item-sampling"></a>Vzorkování referenční položky

Každé přiřazení kvality musí odkazovat na vzorkování položky. Vzorkování položky definuje množství, které bude odesláno pro řízení kvality. Může být nastavena tak, aby se použila pouze na přidružení kvality, kde hodnta **Použitelný typ skladu** je _Pouze správa kvality pro procesy skladu_. Pokud hodnota **Rozsahu vzorkování** pro vzorkování položky je _Náklad_ nebo _Zásilka_ nebo pokud je hodnota **Určení množství** je _Úplná registrační značka_, může být vzorkování položky odkazováno pouze přiřazeními kvality, kde hodnota **Použitelný typ skladu** je _Pouze správa kvality pro procesy skladu_.

Pokud definujete vzorkování položky, které používá použitelný typ skladu _Pouze správa kvality pro procesy skladu_, zobrazí se chybová zpráva, pokud se na ni pokusíte odkázat z přidružení kvality, které nepoužívá funkci _Pouze správa kvality pro procesy skladu_.

> [!NOTE]
> Vzorkování zboží, které používá úplné blokování, není podporováno pro přiřazení kvality, kde je pole **Použitelný typ skladu** nastaveno na _Pouze správa kvality pro procesy skladu_.

### <a name="item-sampling"></a>Vzorkování položky

Vzorkování zboží určuje, jak často jsou položky odesílány pro řízení kvality. Funkce _Správa kvality pro procesy skladu_ zavádí pojem _rozsah vzorkování položek_. Systém používá obor vzorkování položky při vyhodnocení, zda a jak by měly být vytvořeny objednávky kvality nebo práce s vzorkováním a pořadí kvality.

Chcete-li nastavit vzorkování položek, přejděte na **Řízení zásob \> Nastavení \> Správa kvality \> Vzorkování položek** a nastavte pole **Rozsah vzorkování** na jednu z následujících hodnot:

- **Objednávka** – Řádek zdrojového dokumentu bude základem pro vyhodnocení, zda a jak se tvoří objednávky kvality nebo práce s vzorkováním a pořadí kvality. Tato hodnota představuje výchozí hodnotu, a když je vybrána, systém pracuje stejným směrem, když není zapnuta funkce _Správa kvality pro skladové procesy_.
- **Náklad** – náklad bude použit jako základ pro vyhodnocení, zda a jak bude vytvořena objednávka kvality nebo práce. Tato hodnota je k dispozici pouze v případě, že je zapnuta funkce _Správa kvality pro procesy skladu_.
- **Zásilka** – zásilky budeou použity jako základ pro vyhodnocení, zda a jak bude vytvořena objednávka kvality nebo práce. Tato hodnota je k dispozici pouze v případě, že je zapnuta funkce _Správa kvality pro procesy skladu_.

> [!NOTE]
> Pokud je pole **Rozsah vzorkování** nastaveno na *Náklad* nebo *Dodávka*, budou použity entity náklad a dodávka, jsou-li k dispozici. Pokud nejsou k dispozici, bude použita entita objednávka.

Funkce _Správa kvality pro procesy skladu_ také zavádí hodnotu *Úplná registrační značka* pro pole **Určení množsví**. Tato hodnota podporuje vytvoření práce objednávky kvality a práci vzorkování položek kvality na základě registračních značek. Vyberete-li tuto hodnotu, dojde k následujícím změnám:

- K dispozici je možnost **Přerušení počítání dle položky** a **Dle n-té registrační značky** na pevné záložce **Proces**.
- Pole **Hodnota** na pevné záložce **Množství vzorkování** nebude k dispozici.
- Možnosti **Dle aktualizovaného množství**, **Umístění** a **Registrační značka** jsou nastaveny na *Ano* a nastavení nelze změnit.

Možnost **Přerušení počítání dle položky** určuje, zda je počet registračních značek hodnocen pro jednu položku nebo pro všechny položky v rozsahu vzorkování. Varianty produktu jsou považovány za stejnou položku. Tato možnost rovněž určuje, zda je u každé položky vynulováno počítání registračních značek.

Hodnota pole **Dle n-té registrační značky** určuje, jak často jsou objednávky kvality vytvářeny ve vztahu k počtu registrovaných položek. Například hodnota *3* odešle každé třetí položce řízení kvality, počínaje první položkou. Hodnota musí být větší než 0 (nula).

Zatímco pracovníci přijímají položky pomocí aplikace skladu, systém ověří, zda je přiřazení kvality nastaveno pro každou příchozí položku. Je-li přidružení kvality nastaveno, systém použije záznam vzorkování položky, který je konfigurován pro toto přiřazení kvality, aby určil, jakým způsobem bude vytvořena objednávka kvality, práce vzorkování položek kvality a práce s nákupními objednávkami.

> [!NOTE]
> Pokud se registrace příjmu provádí ve webovém klientovi (pomocí stránky malého registračního záznamu nebo deníku doručení položky pro řádky nákupní objednávky), nebude vytvořena žádná práce vzorkování položky kvality nebo práce s nákupní objednávkou bez ohledu na nastavení. Pro položky, které odpovídají přidružení kvality, se místo vzorkování položky použije pro řízení vytváření objednávek kvality.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Příklady automatického generování objednávek kvality

Následující příklady ukazují, jak nastavení přiřazení kvality a související vzorkování položky ovlivňují generování objednávek kvality v případě, že je pole **Použitelný typ skladu** nastaveno na _Pouze správa kvality pro procesy skladu_.

Pokud je hodnota **Určení množství** _Úplná registrační značka_, pole **Dle n-té registrační značky** určuje, pro které je vytvořena práce vzorkování položky kvality. První regitrační značka se vždy řídí řízením kvality a hodnota tohoto pole určuje, že je nutné, aby každá *n-tá* registrační značka byla odeslána.

Hodnota **Referenční typ** pro následující příklady je _Nákup_ a **Typ události** je *Registrace*.

| Rozsah vzorkování | Určení množství | Na aktualizované množství | Na dimenzi úložiště | Rozčlenit počet podle zboží | Každá n-tá registrační značka | Výsledek |
|---|---|---|---|---|---|---|
| Objednat | Úplná registrační značka | Ano _(uzamčeno/nelze upravovat)_ | <p>Skladové místo: Ano</p><p>Registrační značka: Ano _(uzamčeno/nelze upravovat)_</p> | Žádný | 3 | <p>**Množství řádku objednávky: 100 EA**</p><ol><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP1<p>Práce pro vzorkování položky kvality pro 20 EA</p><p>Objednávka kvality 1 na 20 EA</p></li><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP2<p>Práce s nákupní objednávkou na 20 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP3<p>Práce s nákupní objednávkou na 20 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP4<p>Práce pro vzorkování položky kvality pro 20 EA</p></li><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP5<p>Práce s nákupní objednávkou na 20 EA (zaskladnění)</p></li></ol> |
| Objednat | Fixní množství = 1 | Ano | <p>Skladové místo: Ano</p><p>Registrační značka: Ano</p> | Žádný | Nelze použít | <p>**Množství řádku objednávky: 100**</p><ol><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP1<p>Práce pro vzorkování položky kvality pro 1 EA</p><p>Objednávka kvality 1 na 1 EA</p><p>Práce s nákupní objednávkou na 19 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP2<p>Práce pro vzorkování položky kvality pro 1 EA</p><p>Objednávka kvality 1 na 1 EA</p><p>Práce s nákupní objednávkou na 19 (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP3<p>Práce pro vzorkování položky kvality pro 1 EA</p><p>Objednávka kvality 1 na 1 EA</p><p>Práce s nákupní objednávkou na 19 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP4<p>Práce pro vzorkování položky kvality pro 1 EA</p><p>Objednávka kvality 1 na 1 EA</p><p>Práce s nákupní objednávkou na 19 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 20 EA, LP5<p>Práce pro vzorkování položky kvality pro 1 EA</p><p>Objednávka kvality 1 na 1 EA</p><p>Práce s nákupní objednávkou na 19 EA (zaskladnění)</p></li></ol> |
| Objednat | Procento = 10 | Žádný | <p>Umístění: Ne</p><p>Registrační značka: Ne</p> | Žádný | Nelze použít | <p>**Množství řádku objednávky: 100 EA**</p><ol><li>Registrace příjmu v aplikaci skladu pro 50 EA, LP1<p>Práce pro vzorkování položky kvality pro 10 EA</p><p>Objednávka kvality 1 na 10 EA</p><p>Práce s nákupní objednávkou na 40 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 50 EA, LP2<p>Práce s nákupní objednávkou na 50 EA (zaskladnění)</p></li></ol> |
| Načíst | Procento = 5 | Ano _(uzamčeno/nelze upravovat)_ | <p>Umístění: Ne</p><p>Registrační značka: Ne</p> | Žádný | Nelze použít | <p>**Množství řádku objednávky: 500 EA**</p><p>**Dva náklady: první náklad 200 EA, druhý náklad 300 EA**</p><ol><li>Registrace příjmu v aplikaci skladu pro první náklad pro 100 EA<p>Práce pro vzorkování položky kvality pro 5 EA</p><p>Objednávka kvality 1 na 5 EA</p><p>Práce s nákupní objednávkou na 95 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro první náklad pro 100 EA<p>Práce pro vzorkování položky kvality pro 5 EA</p><p>Objednávka kvality 1 na 5 EA</p><p>Práce s nákupní objednávkou na 95 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro druhý náklad pro 300 EA<p>Práce pro vzorkování položky kvality pro 15 EA</p><p>Objednávka kvality 1 na 15 EA</p><p>Práce s nákupní objednávkou na 285 EA (zaskladnění)</p></li></ol> |
| Objednat | Procento = 10 | Žádný | <p>Skladové místo: Ano</p><p>Registrační značka: Ano</p> | Žádný | Nelze použít | <p>**Množství řádku objednávky: 100**</p><ol><li>Registrace příjmu v aplikaci skladu pro 50 EA, LP1<p>Práce pro vzorkování položky kvality pro 5 EA</p><p>Objednávka kvality 1 na 5 EA</p><p>Práce s nákupní objednávkou na 45 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 50 EA, LP2<p>Práce pro vzorkování položky kvality pro 5 EA</p><p>Objednávka kvality 1 na 5 EA</p><p>Práce s nákupní objednávkou na 45 (zaskladnění)</p></li></ol> |
| Načíst | Úplná registrační značka | Ano _(uzamčeno/nelze upravovat)_ | <p>Skladové místo: Ano</p><p>Registrační značka: Ano _(uzamčeno/nelze upravovat)_</p> | Žádný | 3 | <p>**Dvě položky:**</p><ul><li>**Množství řádku objednávky pro položku A: 120 EA (4 palety)**</li><li>**Množství řádku objednávky pro položku B: 90 EA (3 palety)**</li></ul><p>**Jeden náklad, dva řádky nakládky s každým řádkem objednávky**</p><ol><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP1<p>Práce pro vzorkování položky kvality pro 30 EA</p><p>Objednávka kvality 1 na 30 EA</p></li><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP2<p>Práce s nákupní objednávkou na 30 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP3<p>Práce s nákupní objednávkou na 30 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP4<p>Práce pro vzorkování položky kvality pro 30 EA</p><p>Objednávka kvality 1 na 30 EA</p></li><li>Registrace příjmu v aplikaci skladu pro položku B, 30 EA, LP5<p>Práce s nákupní objednávkou na 30 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro položku B, 30 EA, LP6<p>Práce s nákupní objednávkou na 30 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP7<p>Práce pro vzorkování položky kvality pro 30 EA</p><p>Objednávka kvality 1 na 30 EA</p></li></ol> |
| Načíst | Úplná registrační značka | Ano _(uzamčeno/nelze upravovat)_ | <p>Skladové místo: Ano</p><p>Registrační značka: Ano _(uzamčeno/nelze upravovat)_</p> | Ano | 3 | <p>**Dvě položky:**</p><ul><li>**Množství řádku objednávky pro položku A: 120 EA (4 palety)**</li><li>**Množství řádku objednávky pro položku B: 90 EA (3 palety)**</li></ul><p>**Jeden náklad, dva řádky nakládky s každým řádkem objednávky**</p><ol><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP1<p>Práce pro vzorkování položky kvality pro 30 EA</p><p>Objednávka kvality 1 na 30 EA</p></li><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP2<p>Práce s nákupní objednávkou na 30 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP3<p>Práce s nákupní objednávkou na 30 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP4<p>Práce pro vzorkování položky kvality pro 30 EA</p><p>Objednávka kvality 1 na 30 EA</p></li><li>Registrace příjmu v aplikaci skladu pro položku B, 30 EA, LP5<p>Práce pro vzorkování položky kvality pro 30 EA</p><p>Objednávka kvality 1 na 30 EA</p></li><li>Registrace příjmu v aplikaci skladu pro položku B, 30 EA, LP6<p>Práce s nákupní objednávkou na 30 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro položku A, 30 EA, LP7<p>Práce s nákupní objednávkou na 30 EA (zaskladnění)</p></li></ol> |
| Načíst | Procento = 10 | Ano _(uzamčeno/nelze upravovat)_ | <p>Umístění: Ne</p><p>Registrační značka: Ne</p> | Žádný | Nelze použít | <p>**Množství řádku objednávky: 100 EA**</p><p>**Nejsou vytvořeny žádné Náklad. Je použit rozsah objednávky.**</p><ol><li>Registrace příjmu v aplikaci skladu pro 50 EA, LP1<p>Práce pro vzorkování položky kvality pro 5 EA</p><p>Objednávka kvality 1 na 5 EA</p><p>Práce s nákupní objednávkou na 45 EA (zaskladnění)</p></li><li>Registrace příjmu v aplikaci skladu pro 50 EA, LP2<p>Práce pro vzorkování položky kvality pro 5 EA</p><p>Objednávka kvality 1 na 5 EA</p><p>Práce s nákupní objednávkou na 45 EA (zaskladnění)</p></li></ol> |

Když pracovník ověří některou z objednávek kvality zobrazených v předchozí tabulce, systém automaticky vygeneruje práci objednávky kvality, která přesune zásoby z místa řízení kvality do umístění, které je definováno v direktivě skladového místa pro typ pracovního příkazu _Objednávka kvality_. Můžete nastavit libovolné skladové místo pro tento účel, jako je například vrácení nebo místo skladování, v závislosti na výsledku testu pro objednávku kvality. Příklad tohoto nastavení naleznete v [ukázkovém scénáři](#example-scenario) na konci tohoto tématu.

Můžete znovu otevřít objednávku kvality, která již byla ověřena, za předpokladu, že práce objednávky kvality, která souvisí s přesunutím skladu z kontroly kvality, nemá hodnotu **Stav práce** *Uzavřeno* nebo *Probíhá*.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Přehled o zpracování, pokud je současně více přidružení kvality

Je možné definovat více přiřazení kvality a použít je na stejný řádek zdrojového dokumentu a pole **Použitelný typ skladu** lze nastavit na _Pouze správa kvality pro procesy skladu_ u některých přiřazení kvality a _Vše_ pro ostatní.

V následujícím příkladu je hodnota **Referenčního typu** nastavena na _Nákup_.

1. První přiřazení kvality je nastaveno následujícím způsobem:

    - **Použitelný typ skladu:** *Pouze správa kvality pro procesy skladu*
    - **Kód položky:** *A0001*
    - **Kód účtu:** *Vše*
    - **Testovací skupina:** *Příloha*
    - **Vzorkování položky:** *5 ks*

1. Druhé přiřazení kvality je nastaveno následujícím způsobem:

    - **Použitelný typ skladu:** *Vše*
    - **Kód položky:** *Vše*
    - **Kód účtu:** *Vše*
    - **Testovací skupina:** *Příloha*
    - **Vzorkování položky:** *1 ks*

1. Třetí přiřazení kvality je nastaveno následujícím způsobem:

    - **Použitelný typ skladu:** *Pouze správa kvality pro procesy skladu*
    - **Kód položky:** *Vše*
    - **Kód účtu:** *104*
    - **Testovací skupina:** *Překážka*
    - **Vzorkování položek:** *Každá druhá registrační značka* (Toto nastavení znamená, že první, třetí, páté atd. přijaté registrační značky vytvoří objednávku kvality.)

1. Čtvrté přiřazení kvality je nastaveno následujícím způsobem:

    - **Použitelný typ skladu:** *Vše*
    - **Kód položky:** *Vše*
    - **Kód účtu:** *Vše*
    - **Testovací skupina:** *Překážka*
    - **Vzorkování položky:** *5 ks*

1. Páté přiřazení kvality je nastaveno následujícím způsobem:

    - **Použitelný typ skladu:** *Vše*
    - **Kód položky:** *Vše*
    - **Kód účtu:** *Vše*
    - **Testovací skupina:** *Kužel*
    - **Vzorkování položek:** *10%*

Pro dodavatele 104 byla nyní vytvořena nákupní objednávka pro množství 10 položek A0001. Poté bude řádek nákupní objednávky s množstvím 10 registrován jako přijatý na jedné registrační značce pomocí aplikace skladu. Zde je výsledek:

- Existuje jedna objednávka kvality od přidružení kvality pro testovací skupinu *Příloha*. Množství je 5. Druhé přidružení kvality neobsahuje žádnou objednávku kvality, protože kritéria pro první přiřazení kvality jsou konkrétnější vzhledem k testovací skupině *Příloha*.
- Existuje jedna objednávka kvality pro třetí přidružení kvality pro testovací skupinu *Překážka*. Množství je 10. Čtvrté přidružení kvality neobsahuje žádnou objednávku kvality, protože kritéria pro první přiřazení kvality jsou konkrétnější vzhledem k testovací skupině *Překážka*.
- Existuje jedna objednávka kvality pro páté přidružení kvality pro testovací skupinu *Kužel*. Množství je 1.

V souvislosti s vytvořením jedné objednávky kvality pro každé ze tří přiřazení kvality je rovněž vytvořena práce vzorkování položky kvality. Registrované množství je pouze 10. Vzhledem k nastavení vzorkování zboží však součet množství objednávky kvality, které jsou vytvořeny pro použitelný typ skladu *Pouze správa kvality pro procesy skladu* je 16, což překračuje fyzické zaregistrované množství 10. Proto se práce nevytvoří pro množství objednávky s plnou kvalitou (16), protože pro pohyb do umístění řízení kvality jsou fyzicky k dispozici pouze 10. Priorita, která se používá k vytvoření vzorkování položky kvality práce, se řídí pořadím vytvoření objednávky kvality:

- **První objednávka kvality (množství = 5):** práce vzorkování položky kvality je vytvořena pro 5. Množství 5 (10 – 5) nyní zůstává pro následnou tvorbu vzorkování položky kvality.
- **Druhá objednávka kvality (množství = 10):** práce vzorkování položky kvality je vytvořena pro 5. Množství 0 (nula) nyní zůstává pro následnou tvorbu vzorkování položky kvality.
- **Třetí objednávka kvality (množství = 1):** není vytvořena žádná práce vzorkování položky kvality.

V rámci procesu vytváření objednávek kvality je vytvořeno blokování zásob s množstvím 10. Toto blokování zásob je odkazováno proti jednotlivým třem objednávkám kvality. Součet množství objednávky kvality je 16.

Při ověření objednávek kvality se systém pokusí vytvořit objednávku kvality pro jednotlivé ověřené objednávky kvality. Vzhledem k tomu, že součet množství objednávky kvality překračuje množství, které je skutečně blokováno a je tedy k dispozici pro vytvoření práce, nelze vytvořit objednávku kvality pro množství objednávky s plnou kvalitou, jak je uvedeno zde. (Tento příklad pokračuje v předchozím příkladu.)

1. **Ověřte druhou vytvořenou objednávku kvality (množství = 10). Je vytvořena práce objednávky kvality pro množství 4.**

    Vytvoření objednávky kvality je aktivováno změnou množství blokování zásob. Vzhledem k tomu, že součet množství objednávky kvality byl 16, ověření množství 10 způsobí, že zbývající množství objednávky kvality bude ověřeno jako rovno 6. Množství blokování zásob je sníženo z hodnoty 10 na hodnotu 6. Snížené množství, které je 4, je přiděleno vytvoření práce objednávky kvality.

2. **Ověřte první vytvořenou objednávku kvality (množství = 5). Je vytvořena práce objednávky kvality pro množství 5.**

    Vytvoření objednávky kvality je aktivováno změnou množství blokování zásob. Vzhledem k tomu, že součet množství objednávky kvality byl 6, ověření množství 5 způsobí, že zbývající množství objednávky kvality bude ověřeno jako rovno 1. Množství blokování zásob je sníženo z hodnoty 6 na hodnotu 1. Snížené množství, které je 5, je přiděleno vytvoření práce objednávky kvality.

3. **Ověřte třetí vytvořenou objednávku kvality (množství = 1). Je vytvořena práce objednávky kvality pro množství 1.**

    Vytvoření objednávky kvality je aktivováno změnou množství blokování zásob. Vzhledem k tomu, že součet množství objednávky kvality byl 1, ověření množství 1 způsobí, že zbývající množství objednávky kvality bude ověřeno jako rovno 0 (nula). Blokování zásob je odebráno (to znamená, že množství blokování zásob se sníží od 1 do 0). Snížené množství, které je 1, je přiděleno vytvoření práce objednávky kvality.

> [!NOTE]
> Vytvoření objednávky kvality závisí na množství blokování zásob, které je odkazováno proti jedné nebo více objednávkám kvality. Pokud součet množství objednávky kvality překročí odkazované množství zásob, bude pořadí, v němž jsou objednávky kvality ověřovány, určovat vytvoření práce objednávky kvality.

## <a name="canceling-quality-item-sampling-work"></a>Storno práce pro vzorkování položky kvality

Můžete zrušit práci vytvořenou pro vzorkování položky kvality. Chcete-li určit, co se stane, když je tato práce zrušena, postupujte podle následujících kroků.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na kartě **Obecné** na pevné záložce **Práce** nastavte možnost **Zrušit registraci příjemky při stornu práce** na jednu z následujících hodnot:

    - **Ano** – Pokud je zrušena práce vzorkování položky kvality, dojde k odstranění související objednávky kvality a zásoby se nezaregistrují.
    - **Ne** – Pokud je zrušena práce vzorkování položky kvality, nedojde k odstranění související objednávky kvality a zásoby se zaregistrují.

## <a name="cross-docking"></a>Cross-docking

Můžete mít nastavení přiřazení kvality, které vytvoří práci vzorkování zboží. Pokud však existuje cross docking s přiřazením kvality, které vytváří práci vzorkování položky kvality, pokud existuje pouze dostatečné množství pro uspokojení cross dockingu, je vytvořena pouze práce vzorkování zboží. V případě, že možnost **Povolit objednávku kvality pro skladové procesy** je nastavena na hodnotu _Ano_ pro přijímací sklad a pole **Použitelný typ skladu** je nastaveno na _Pouze správa kvality pro procesy skladu_ pro přiřazení kvality, vytvoření vzorkování položky kvality má přednost před vytvořením funkce cross dockingu. Pokud množství překročí požadavek pro cross docking, systém stále vytvoří pouze práci vzorkování položky.

## <a name="destructive-testing"></a>Destruktivní testování

Můžete definovat skupinu testů, která provádí destruktivní testování. V případě destruktivního testu je předpokladem, že bez ohledu na výsledek testu bude v rámci testu zničeno množství testované položky. Postup, jakým funkce _Správa kvality pro procesy skladu_ podporuje destruktivní testování, připomíná způsob, jakým jej správa kvality podporuje, pokud tato funkce není zapnuta. Před ověřením objednávky kvality musí kontrolor kvality specifikovat skladové místo výdeje pro množství, které bylo zničeno. Výdej můžete zaregistrovat na stránce objednávka kvality výběrem možnosti **Zásoby \> Vyskladnit** v podokně akcí. Po zaregistrování výdeje pro množství objednávky kvality lze ověření dokončit.

## <a name="example-scenario"></a>Příklad

### <a name="prepare-the-scenario"></a>Příprava scénáře

Chcete-li tento scénář použít, je nutné připravit systém následujícím způsobem:

- Zkontrolujte, zda jsou v systému nainstalována ukázková data, a vyberte právnickou osobu **USMF**.
- Zapněte funkci _Správa kvality pro procesy skladu_ ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Nakonfigurujte sklad 51 pro použití funkce _Správa kvality pro procesy skladu_ pomocí následujících kroků:

    1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
    1. Vyberte sklad 51.
    1. Na pevné záložce **Sklad** nastavte možnost **Povolit objednávku kvality pro skladové procesy** na *Ano*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Nastavení kvality – přejde do umístění kontroly kvality

Nyní je nutné připravit základní nastavení, které umožní systému podporovat funkci _Správa kvality pro procesy skladu_ pro sklad 51. (Ukázková data definují umístění správy kvality s názvem *QMS.* Toto umístění je v tomto scénáři popsáno několikrát.) Připravujete následující prvky, jak je popsáno v pododdílech tohoto oddílu:

- Pracovní třída
- Šablona práce
- Směrnice skladového místa
- Vzorkování položky
- Přiřazení kvality
- Položky nabídky mobilního zařízení

#### <a name="work-class-for-quality-in"></a>Třída práce pro kvalitu

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.
1. Vytvořte třídu práce a nastavte následující hodnoty:

    - **ID pracovní třídy:** _QualityIn_
    - **Popis** _Vzorkování položky kvality_
    - **Typ pracovního příkazu:** _Vzorkování položky kvality_

#### <a name="work-template"></a>Šablona práce

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. Nastavte hodnotu v poli **Typ pracovního příkazu** na _Vzorkování položky kvality_.
1. Vytvořte pracovní šablonu a nastavte následující hodnoty:

    - **Šablona práce:** _51 kvalita_
    - **Popis šablony práce:** _51 kvalita_

1. Přidejte řádek do pracovní šablony a nastavte následující hodnoty:

    - **Typ práce:** _Výdej_
    - **ID pracovní třídy:** _QualityIn_

1. Přidejte druhý řádek do pracovní šablony a nastavte následující hodnoty:

    - **Typ práce:** _Vložit_
    - **ID pracovní třídy:** _QualityIn_

#### <a name="location-directive"></a>Směrnice skladového místa

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. Nastavte hodnotu v poli **Typ pracovního příkazu** na _Vzorkování položky kvality_.
1. Vytvořte směrnici pracovního místa a nastavte následující hodnoty:

    - **Název:** _51 do kvality_
    - **Typ práce:** _Vložit_
    - **Lokalita:** 5
    - **Sklad:** _51_

1. Přidejte řádek pro směrnici skladového místa a nastavte následující hodnoty:

    - **Od množství:** _1_
    - **Do množství:** _1000000_

1. Vytvořte akci směrnice pracovního místa a nastavte následující hodnotu:

    - **Název:** _Kvalita_

1. Pro akci nové směrnice skladového místa vyberte **Upravit dotaz** a zadejte záznam **Rozsahu** s následujícími hodnotami:

    - **Tabulka:** *umístění*
    - **Pole:** _ID profilu skladového místa_
    - **Kritéria:** *QMS*

1. Chcete- li uložit dotaz a uložit novou směrnici skladového místa, klepněte na tlačítko **OK**.

Dále je nutné změnit pořadí existujících direktiv umístění pro sklad 51. Ukázková data zahrnují dvě direktivy skladových míst, které mají hodnotu **Typ pracovního příkazu** _Nákup_: jedna s názvem _51 QMS_ a druhá s názvem _51 PO Direct_. Chcete-li zajistit, aby pro sklad 51 byla použita funkce *Správa kvality pro procesy skladu*, je nutné zajistit, aby nebyla použita směrnice skladového místa _51 QMS_. Avšak namísto odstranění této direktivy umístění (protože ji budete chtít použít v budoucnu) můžete pouze změnit sekvenci.

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. Nastavte pole **Typ pracovního příkazu** na _Nákupní objednávka_.
1. V seznamu pořadí vyberte pro direktivu skladového místa _51 PO Direct_ pořadové číslo 5.
1. Přesune vybranou sekvenci nahoru na pořadové číslo 4.
1. Ověřte, že pořadové číslo směrnice umístění _51 QMS_ je nyní alespoň 5.

#### <a name="item-sampling"></a>Vzorkování položky

Funkce _Správa kvality pro procesy skladu_ přidává některé nové možnosti vzorkování zboží. Hodnota **Rozsah vzorkování** teď může být _Objednávka_, _Zásilka_ nebo _Náklad_ a **Množství vzorkování** může být _Úplná registrační znčka_.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Vzorkování položek**.
1. Vytvořte záznam vzorkování položky a nastavte následující hodnoty:

    - **Vzorkování zboží:** _třetí LP_
    - **Popis:** _každá třetí registrační značka_
    - **Rozsah vzorkování:** _Objednávka_

1. Na pevné záložce **Množství vzorkování** nastavte pole **Určení množství** na _Úplná registrační znčka_.
1. Na pevné záložce **Proces** nastavte pole **Dle n-té registrační značky** na _3_.
1. V části **Dle velikosti skladu** povolte **Sklad** i **Stav zásob**.

#### <a name="quality-associations"></a>Přiřazení kvality

Vytvořte přidružení kvality, které bude používat nové vzorkování položky.

1. Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Přiřazení kvality**.
1. Vytvořte záznam přidružení kvality a nastavte následující hodnoty:

    - **Typ odkazu:** _nákup_
    - **Kód položky:** _tabulka_
    - **Položka:** _M9201_
    - **Lokalita:** _5_

1. Na pevné záložce **Proces** nastavte pole **Typ události** na *Registrace*.
1. Na pevné záložce **Podmínky** nastavte pole **Použitelný typ skladu** na *Pouze správa kvality pro procesy skladu*.
1. Na záložce **Proces objednávky kvalityí** nastavte pole **Zásady zpracování kvality** na _Vytvoření objednávky kvality_.
1. Na pevné záložce **Specifikace** klikněte pravým tlačítkem myši do pole **Testovací skupina** a poté výběrem možnosti **Zobrazit podrobnosti** otevřete stránku **Testovací skupiny**.
1. Na stránce **Testovací skupiny** na kartě **Přehled** horní mřížky vytvořte testovací skupinu a nastavte následující hodnoty:

    - **Testovací skupina:** _QMS_
    - **Popis:** _QMS test_
    - **Přijatelné množství:** _100_
    - **Vzorkování zboží:** _třetí LP_ (Vybrat)

1. Na kartě **Přehled** v dolní mřížce přidejte záznam pro jeden test a nastavte následující hodnoty:

    - **Posloupnost:** *1*
    - **Zkouška:** *Měření skříně*

1. Na kartě **Test** dolní mřížky nastavte následující hodnoty:

    - **Testovací proměnné:** *úspěšné/neúspěšné*
    - **Výchozí výsledek:** *úspěšné*

1. Uložte novou testovací skupinu a zavřete stránku **testovací skupiny**.
1. Zpět na stránce **Přidružení kvality** v poli **Testovací skupina** vyberte **QMS**.
1. Uložte záznam.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Položky nabídky mobilního zařízení pro kvalitu

Chcete-li dokončit nastavení a přesunout zboží do umístění pro řízení kvality, je nutné, aby byla k dispozici vzorkování položky kvality z položky nabídky mobilního zařízení.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. Vyberte položku nabídky mobilního zařízení **Nákupní vyskladnění**.
1. Na pevné záložce **Pracovní třídy** přidejte ID pracovní třídy *QualityIn*.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Souhrn: vaše nastavení pro přesun zboží do řízení kvality

Nyní jste definovali přidružení kvality, které používá funkci *Správa kvality pro skladové procesy* ke spuštění vytvoření objednávky kvality. Pro sklad 51 jste nastavili data práce a místa, aby se zajistilo, že bude vytvořena určitá práce, když se registrace nákupu provede pro položku M9201. Toto nastavení zajišťuje, aby každá třetí registrační značka byla přesunuta do umístění kvality (_QMS_) a aby byla pro množství řidičského průkazu vytvořena objednávka kvality. Všechno ostatní bude přesunuto do zaskladnění namísto místa kontroly kvality.

### <a name="process-quality-management-work"></a>Práce procesů správy kvality

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Vytvořte nákupní objednávku a nastavte následující hodnoty:

    - **Zadejte účet dodavatele:** *104*
    - **Sklad:** *51*

1. Přidejte řádek nákupní objednávky a nastavte následující hodnoty:

    - **Položka:** *M9201*
    - **Množství:** *20*
    - **UoM:** *ea*
    - **Sklad:** *51*

1. Poznamenejte si číslo nákupní objednávky, aby bylo možné je později použít.
1. Přejděte na mobilní zařízení nebo emulátor, ve kterém je spuštěná aplikace skladu, a přihlaste se do skladu 51 pomocí *51* jako ID uživatele a *1* jako heslo.
1. Přejděte na **Vstupní \> Příjem nákupu** a zadejte následující hodnoty:

    - **PONum:** číslo nákupní objednávky, kterou jste vytvořili
    - **Množství:** *5*
    - **Jednotka:** *EA*

1. Pokračujte v příjmu proti řádku, *5 EA*, do úplného přijetí řádku. (Bude vytvořen celkový počet čtyř registračních značek.)
1. Odhlaste se z aplikace skladu.
1. Zpět ve webovém klientovi přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Vyhledejte a otevřete nákupní objednávku.
1. V části **Řádky nákupní objednávky** vyberte řádek pro číslo položky *M9201* a poté vyberte **Řádky nákupní objednávky \> Pracovní podrobnosti**.
1. Všimněte si, že druhá a třetí záhlaví práce, která byla vytvořena, jsou běžná práce na skladě, zatímco první a čtvrtá záhlaví práce představují kvalitu práce vzorkování položky. Výsledek je v souladu s nastavením vzorkování zboží, které je nakonfigurováno pro každou třetí registrační značku.

#### <a name="move-to-the-quality-control-location"></a>Přesunout do umístění kontroly kvality

Nyní budete přemísťovat registrační desky do jejich určených umístění. První a čtvrtá registrační deska se budou nacházet v umístění kontroly kvality, zatímco druhá a třetí registrační deska budou přímo přecházet do úložiště.

1. Přejděte na mobilní zařízení nebo emulátor, ve kterém je spuštěná aplikace skladu, a přihlaste se do skladu 51 pomocí *51* jako ID uživatele a *1* jako heslo.
1. Přejděte ke **vstupní \> Nákupní zaskladnění** a zaškrtnete všechny registrační značky z předchozího postupu, dokud neukončíte veškerou práci.

#### <a name="summary-process-quality-management-work"></a>Souhrn: Práce procesů správy kvality

Nyní jste spustili práci vzorkování položky kvality pro první a čtvrtou registrační desku tím, že je přesunete do umístění kontroly kvality. Dále jste vyskladnili druhou a třetí registrační značku. Dalším krokem je provedení testování a řízení objednávky kvality.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Nastavení kvality: přesunout z umístění kontroly kvality na místo uložení nebo vrácení

Když zaměstnanci vykazují výsledky objednávky kvality, systém automaticky vygeneruje práci.

Nyní budete pokračovat s požadovaným základním nastavením třídy práce, šablony práce a směrnice skladových míst, aby byla povolena Správa kvality pro skladové procesy, aby bylo možné vytvořit požadovanou práci pro přesunutí množství objednávky kvality z místa řízení kvality do určeného skladového místa.

#### <a name="work-class-for-quality-out"></a>Třída práce pro výstupní kvalitu

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.
1. Vytvořte třídu práce a nastavte následující hodnoty:

    - **ID pracovní třídy:** *QualityOut*
    - **Popis:** *výstupní kvalita*
    - **Typ pracovního příkazu:** *objednávka kvality*

#### <a name="work-templates"></a>Šablony práce

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. Změňte hodnotu **Typu pracovního příkazu** na *Objednávku kvality*.
1. Vytvořte pracovní šablonu a nastavte následující hodnoty:

    - **Šablona práce:** *51 výstupní kvalita*
    - **Popis šablony práce:** *51 výstupní kvalita*

1. Přidejte řádek a nastavte následující hodnoty:

    - **Typ práce:** *Výdej*
    - **ID pracovní třídy:** **QualityOut**

1. Přidejte druhý řádek a nastavte následující hodnoty:

    - **Typ práce:** *Vložit*
    - **ID pracovní třídy:** *QualityOut*

#### <a name="location-directives"></a>Směrnice skladového místa

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. Změňte hodnotu **Typu pracovního příkazu** na *Objednávku kvality*.
1. Vytvořte směrnici pracovního místa a nastavte následující hodnoty:

    - **Název:** *51 průchod*
    - **Typ práce:** *Vložit*
    - **Lokalita:** *5*
    - **Sklad:** *51*

1. V podokně akcí zvolte **Upravit dotaz** a otevřete dialogové okno editor dotazů.
1. Na kartě **Rozsah** natavte následující hodnoty:

    - **Tabulka:** *Objednávky kvality*
    - **Pole:** *stav*
    - **Kritéria:** *předat*

1. Vyberte **OK**, uložte dotaz a zavřete dialogové okno.
1. Na pevné záložce **Řádky** přidejte řádek a nastavte následující hodnoty:

    - **Od množství:** *1*
    - **Do množství:** *1000000*

1. Na pevné záložce **Akce směrnice skladového místa** přidejte řádek a nastavte následující hodnotu:

    - **Název:** *Průchod*

1. Na pevné záložce **Akce směrnice skladového místa** vyberte **Upravit dotaz** a otevřete dialogové okno editor dotazů.
1. Na kartě **Rozsah** natavte následující hodnoty:

    - **Tabulka:** *umístění*
    - **Pole:** *ID zóny*
    - **Kritéria:** *hromadné*

1. Vyberte **OK**, uložte dotaz a zavřete dialogové okno.
1. V podokně akcí vyberte **Uložit** a uložte novou směrnici skladového místa.
1. Vytvořte druhou směrnici pracovního místa a nastavte následující hodnoty:

    - **Název:** *51 selhání*
    - **Typ práce:** *Vložit*
    - **Lokalita:** *5*
    - **Sklad:** *51*

1. V podokně akcí zvolte **Upravit dotaz** a otevřete dialogové okno editor dotazů.
1. Na kartě **Rozsah** natavte následující hodnoty:

    - **Tabulka:** *Objednávky kvality*
    - **Pole:** *stav*
    - **Kritéria:** *neúspěšné*

1. Vyberte **OK**, uložte dotaz a zavřete dialogové okno.
1. Na pevné záložce **Řádky** přidejte řádek a nastavte následující hodnoty:

    - **Od množství:** *1*
    - **Do množství:** *1000000*

1. Na pevné záložce **Akce směrnice skladového místa** přidejte řádek a nastavte následující hodnotu:

    - **Název:** *Selhání*

1. Na pevné záložce **Akce směrnice skladového místa** vyberte **Upravit dotaz** a otevřete dialogové okno editor dotazů.
1. Na kartě **Rozsah** natavte následující hodnoty:

    - **Tabulka:** *umístění*
    - **Pole:** *ID zóny*
    - **Kritéria:** *vrácení*

1. Vyberte **OK**, uložte dotaz a zavřete dialogové okno.
1. V podokně akcí vyberte **Uložit** a uložte novou směrnici skladového místa.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Položky nabídky mobilního zařízení pro výstupní kvalitu

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. Vyberte položku nabídky mobilního zařízení **QMS vyskladnění**.
1. Na pevné záložce **Pracovní třídy** přidejte ID pracovní třídy *QualityPut*.

Pracovníci skladu budou nyní moci vyskladnit práci s objednávkou kvality pomocí položky nabídky **QMS vyskladnění**. Zboží, které selhalo pro řízení kvality, lze vložit do místa vrácení a zboží, které bylo dodáno, lze vložit do umístění hromadného 001.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Souhrn: vaše nastavení pro přesun zboží z řízení kvality

Pro sklad 51 jste nastavili data práce a místa, aby se zajistilo, že bude automaticky vytvořena práce, když se dokončí objednávky kvality. Toto nastavení zajišťuje, aby byla každá registrační značka řízená kvalitou přesunuta do hromadného umístění nebo na místo vrácení.

### <a name="process-quality-management-work"></a>Práce procesů správy kvality

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.
1. Vyberte první objednávku kvality pro zaregistrovaná množství.
1. Vyberte **Ověřit**. Stav testu bude aktualizován na hodnotu *Selhání*.
1. Přejděte do **Řízení skladu \> Všechny práce**.
1. Otevřete právě vytvořenou práci a všimněte si, že hodnota **Typu pracovního příkazu** je *Objednávka kvality*. Práce zahrnuje řádek, na kterém je skladové místo *Vráceno* a stav je *Neúspěšný*. (Pokud byl stav objednávky kvality *Úspěch*, místo uložení bude místo toho *Hromadné* .)
1. Přejděte zpět na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.
1. Vyberte druhou objednávku kvality pro zaregistrované položky.
1. Vyberte **výsledky** nad dolní mřížkou. Aktualizujte hodnotu **Výsledné množství** na *5* a zkontrolujte, zda je hodnota **Výsledku testu** změněna na zaškrtnutí.
1. Zvolte **Ověřit** a zavřete stránku.
1. Zpět na stránce **Objednávky kvality** vyberte možnost **Ověřit** a proveďte ověření. Stav je aktualizován na stav *Úspěch*.

    > [!NOTE]
    > Událost ověření spustí vytvoření pracovní objednávky kvality, která přesune množství z místa řízení kvality do nového umístění.

1. Přejděte do **Řízení skladu \> Všechny práce**.
1. Vyberte právě vytvořenou práci a Všimněte si, že byla vytvořena druhá hlavička pracovního místa, kde skladové místo je *BULK-001*.
1. Přejděte na mobilní zařízení nebo emulátor, ve kterém je spuštěná aplikace skladu, a přihlaste se do skladu 51 pomocí *51* jako ID uživatele a *1* jako heslo.
1. Přejděte na **Kvalita \> Vyskladnění z QMS** a zpracujte každou ze dvou registračních značek, které souvisejí s oběma pracovišti, aby byla uzavřena veškerá práce.

> [!NOTE]
> Zvažte přidání položky kvality do položky nabídky mobilního zařízení, kde je zobrazen kód aktivity *Zobrazit otevřený seznam úkolů*. Příklad naleznete v položce nabídky mobilního zařízení s názvem **Pracovní seznam** v ukázkových datech. Nejprve přidejte třídu práce *Objednávka kvality* do uživatelem řízené položky nabídky, protože tato třída práce je požadována pro práci, která se má zobrazit v pracovním seznamu. Poté přidejte pracovní třídu *Objednávka kvality* do položky nabídky **Pracovní seznam**. Uživatelé, kteří mají přístup k pracovnímu seznamu, budou moci vyskladnit a zpracovat práci, která je automaticky generována ověřením objednávky kvality.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]