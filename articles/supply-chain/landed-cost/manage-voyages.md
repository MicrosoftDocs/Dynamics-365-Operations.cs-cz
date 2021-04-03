---
title: Správa cest
description: Toto téma popisuje, jak pracovat s cestami. Cesta obvykle představuje plavidlo. V závislosti na vašich zvycích a postupech však může představovat dodavatele, nákupní objednávku nebo jinou položku, která má pro vaši organizaci smysl.
author: sherry-zheng
manager: tfehr
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 850fbb2077a592ec4ba8578cab4795d573464f54
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500999"
---
# <a name="manage-voyages"></a>Správa cest

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Cesta obvykle představuje plavidlo. V závislosti na vašich zvycích a postupech však může představovat dodavatele, nákupní objednávku nebo jinou položku, která má pro vaši organizaci smysl.

Stránka **Všechny cesty** poskytuje podrobnosti o cestě, informace o dodání a kalkulaci nákladů, a informace o položkách, nákupních objednávkách a převodních příkazech. Chcete-li otevřít stránku **Všechny cesty** přejděte na **Náklady za doručení \> Cesty \> Všechny cesty**. Tato stránka zobrazuje seznam všech aktuálních cest. Pomocí tlačítek v podokně akcí můžete vytvářet či odstraňovat cesty a pracovat s nimi. Výběrem libovolné cesty v seznamu zobrazte její podrobnosti.

> [!NOTE]
> Přepravní kontejnery a folia jsou spojeny s cestou. Řádky nákupu jsou spojeny s přepravním kontejnerem. Pokud jsou přepravní kontejnery a folia vypnuty, lze je také přímo propojit s cestou. Kromě toho jsou zde zadané náklady rozděleny na všechny připojené řádky nákupu.

## <a name="action-pane"></a>Podokno akcí

Podokno akcí na stránce **Cesty** poskytuje tlačítka, která vám umožní pracovat s vybranou cestou. Každé tlačítko provádí jednu akci. Podokno akcí také obsahuje karty, z nichž každá zase poskytuje sadu souvisejících tlačítek. Není-li uvedeno jinak, jsou všechna tlačítka a karty k dispozici jak v zobrazení seznamu na stránce **Všechny cesty**, tak v podrobném zobrazení pro jednu vybranou cestu.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Tlačítka, která se zobrazují přímo v podokně akcí

V následující tabulce jsou popsána tlačítka, která jsou k dispozici přímo v podoknu akcí.

| Tlačítko | popis |
|---|---|
| Nová | Vytvoří cestu. <!-- KFM: Link to scenario --> |
| Odstranit | Odstraní aktuální cestu. Odstranit lze pouze cesty, které mají stav *Potvrzeno*. Poté, co cesta opustí přístav a zpracuje přepravované zboží, není možné ji odstranit. |
| Editor cesty | Otevře stránku **Editor cesty**, kde můžete přidat nebo odebrat řádky nákupu pro cestu, vytvořit nové kontejnery a upravit podrobnosti samotné cesty. |
| Náklady na cestu | Otevře stránku **Náklady na cestu**, kde si můžete prohlédnout a přidat náklady na úrovni cesty ke všemu zboží na cestě. Když jsou náklady na cestu ručně přidány do cesty, automaticky se přidají do stránky **Dotaz na náklady** a rozdělí se ke každému zboží podle metody, která je uvedena na stránce **Náklady na cestu**. |

### <a name="buttons-on-the-voyage-tab"></a>Tlačítka na kartě Cesta

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na kartě **Cesta** podokna akcí. Tato karta je k dispozici, pouze pokud pracujete v zobrazení seznamu stránky **Všechny cesty**.

| Tlačítko | popis |
|---|---|
| Přepravní kontejner | Otevře stránku, která zobrazuje všechny přepravní kontejnery spojené s vybranou cestou. Může to být jeden kontejner nebo více kontejnerů. |
| Folio | Otevře stránku, která zobrazuje všechna folia spojená s vybranou cestou. Může to být jedno folio nebo více folií. |

### <a name="buttons-on-the-manage-tab"></a>Tlačítka na kartě Správa

V následující tabulce jsou popsány akce, které jsou k dispozici na kartě **Spravovat** podokna akcí.

| Tlačítko | popis |
|---|---|
| Přijaté dokumenty | Aktualizuje cestu, aby byla možnost **Doklady přijaty** nastavena na *Ano*. Toto tlačítko můžete použít k uzamčení položky nebo řádku nákupu, aby ji nebylo možné dále aktualizovat. |
| Na cestě | Aktualizuje pole **Stav cesty** na stav při přepravě, který je stanoven na stránce **[Parametry nákladů za doručení](landed-cost-parameters.md)**. Tento proces nemá žádnou další logiku. Cestu lze také automaticky aktualizovat na stav při přepravě na základě nastavení v [řídicím centru sledování](delivery-information-setup.md).
| Připraveno k výpočtu nákladů | Aktualizuje pole **Stav cesty** na stav připravenosti k výpočtu nákladů, který je stanoven na stránce **[Parametry nákladů za doručení](landed-cost-parameters.md)**. Cesta může být oceněna, když jsou zpracovány všechny faktury (skladové faktury i faktury za náklady na cestu) a bylo přijato zboží. Pokud odhadované náklady spojené s cestou nebyly oceněny, dojde k chybě při pokusu o zpracování ocenění cesty. |
| Nacenění nákladů | Odstraňte případné nesrovnalosti ve výpočtu nákladů poté, co u všech nákupních objednávek a nákladů na cestu existuje faktura. Když vyberete toto tlačítko, zobrazí se dialogové okno **Aktualizace cesty – Oceněno**. V něm si můžete vybrat zaúčtování ve standardní finanční datum nebo zadat datum zaúčtování a poté akci spustit. Akci můžete spustit tolikrát, kolikrát chcete. Dialogové okno **Aktualizace cesty – Oceněno** můžete také použít k vytvoření plánu spuštění akce jako periodické úlohy (dávková úloha). Doporučujeme akci pravidelně spouštět jejím nastavením jako dávkové úlohy. |
| Zaúčtovat příjemky | Zaúčtuje seznam příjemek pro všechny řádky nákupní objednávky v cestě. Pokud se používají cesty s více společnostmi, otevře se pro každou společnost nové dialogové okno účtování seznamu příjemek, které musí být zpracováno v každé právnické osobě. |
| Zaúčtovat příjemku produktu | Zaúčtuje příjemku produktu pro všechny řádky nákupní objednávky v cestě. Proces přijetí produktu pro řádky nákupní objednávky, které jsou spojeny s cestou, bude použit pouze v případě, že zboží **neprojde** zpracováním přepravovaného zboží. Pokud zboží projde zpracováním přepravovaného zboží, zobrazí se při pokusu o zaúčtování příjemky produktu na řádku nákupní objednávky chyba. Pokud se používají cesty s více společnostmi, otevře se pro každou společnost dialogové okno účtování nové poznámky k dodání. |
| Zaúčtovat fakturu | Zaúčtuje fakturu pro všechny řádky nákupní objednávky v cestě. Pokud zboží na cestě projde zpracováním přepravovaného zboží, budou řádky nákupní objednávky fakturovány před dokončením procesu přijímání. Při fakturaci původní nákupní objednávky budou vytvořeny objednávky přepravovaného zboží, které jsou přidruženy k řádkům původní nákupní objednávky. Tyto objednávky pak může přijmout sklad. Pokud se používají dodávky s více společnostmi, otevře se pro každou společnost nové dialogové okno účtování faktury. |
| Převodní příkaz expedice | Zaúčtuje cestu převodního příkazu pro všechny řádky nákupní objednávky v cestě. Pokud je toto tlačítko vybráno, budou možné aktualizovat pouze převodní příkazy. |
| Přijmout převodní příkaz | Zaúčtuje příjemku převodního příkazu pro všechny řádky nákupní objednávky v cestě. |
| Přijmout přepravované zboží | Přijme všechny řádky objednávky, které jsou v cestě přepravovány. Toto tlačítko je jednou ze tří možností, které jsou k dispozici pro příjem přepravovaného zboží na cestě. (Další dvě možnosti jsou tlačítko **Vytvořit deník doručení**, které je popsáno dále v této tabulce, a skladová aplikace.) Tato možnost je nejjednodušší a bude zpracovávat přepravované zboží z tranzitního skladu do konečného cílového skladu. Chcete-li mít nad procesem větší kontrolu, použijte ke zpracování příjmu zboží deník příjezdu nebo mobilní zařízení. |
| Najít automatické náklady | Najde jakékoli příslušné náklady na cestu. Pokud tyto náklady již byly nalezeny nebo aktualizovány, zobrazí se následující zpráva: „Existují nevyfakturované řádky nákladů. Chcete je přepsat?“ Budou nalezeny veškeré náklady, které nebyly spojeny s cestou v době vytvoření. Náklady na cestu, které jsou spojené s cestou a byly fakturovány, nebudou přepsány. |
| Vytvořit deník doručení | <p>Otevře dialogové okno **Vytvořit deník doručení**, kde můžete vytvořit deník doručení, který určuje umístění. Dialogové okno nabízí následující možnosti:</p><ul><li>**Vytvořit z přepravovaného zboží** nebo **Vytvořit z převodního příkazu** – Popisek pro tuto možnost se mění v závislosti na tom, zda používáte proces přepravovaného zboží. Nastavením na *Ano* otevřete stránku deníku doručení, která vám umožní zpracovat standardní deník doručení pro přepravované zboží, které je spojeno s cestou. Pokud položka již byla přijata do konečného cílového skladu, nebude přidána do řádků deníku doručení.</li><li>**Inicializovat množství** – Nastavte tuto možnost na *Ano*, chcete-li inicializovat množství, které bude přijato, na základě množství zboží uvedeného na řádku cesty. Pokud byl řádek cesty částečně přijat, bude toto množství zbývajícím množstvím. Doporučujeme nastavit tuto možnost na *Ano*.</li><li>**Vytvořit z řádků objednávky** – Nastavte tuto možnost na *Ano*, chcete-li převzít hodnotu z řádků objednávky.</li></ul><p>Toto tlačítko je jednou ze tří možností, které jsou k dispozici pro příjem zboží na cestě. (Další možnosti jsou tlačítko **Přijmout přepravované zboží**, které bylo popsáno dříve v této tabulce, a skladová aplikace.)</p> |
| Časově rozlišené náklady | Můžete shromáždit náklady, když má typ nákladů pro debet zadaný účet hlavní knihy. Toto tlačítko se obvykle používá, když je zboží na cestě, nebo když bylo zboží přijato a fakturováno. |
| Agregovat náklady | Přesune náklady z úrovně přepravního kontejneru na úroveň cesty. Toto tlačítko můžete použít ve scénáři sdílených služeb/přepravy, kde více entit sdílí přepravní kontejner nebo prostor kartonu. Například cesta má přepravní kontejner o délce 40 stop a přepravní kontejner o délce 20 stop a rozdělení se provádí podle objemu. V takovém případě může být penalizováno zboží/entity které sdílejí nebo využívají prostor ve 20stopovém přepravním kontejneru. Pro spravedlivé rozdělení nákladů mohou některé organizace chtít převést náklady na cestu a rozdělit je na základě metody rozdělení na úrovni cesty. |
| Změnit šablonu cesty | Otevřete dialogové okno, ve kterém můžete změnit šablonu cesty. Po změně šablony budou náklady na cestu odstraněny. Možná budete muset vybrat příkaz **Najít automatické náklady** (viz popis výše v této tabulce) nebo znovu ručně přidat náklady. |

### <a name="buttons-on-the-general-tab"></a>Tlačítka na kartě Obecné

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na kartě **Obecné** podokna akcí.

| Tlačítko | popis |
|---|---|
| Příjemka | Otevře seznam příjemek produktu pro všechny řádky nákupní objednávky v cestě. Pokud se používají cesty s více společnostmi, otevře se pro každou společnost nový seznam příjemek. Pokud nebyly zpracovány žádné seznamy příjemek produktů, toto tlačítko není k dispozici. |
| Příjemka produktu | Otevře záznam příjmu produktu pro řádky nákupní objednávky, které jsou spojeny s cestou, pokud je tento záznam použit. Pokud nebyly zaúčtovány žádné příjemky produktů, toto tlačítko není k dispozici. Proces příjmu produktu nebude použit, pokud používáte zpracování přepravovaného zboží. |
| Doručení položky | Otevře deník doručení zboží, pokud je použit. |
| Sledování | Otevře stránku **Sledování vstupu**, kde můžete aktualizovat očekávané datum příjezdu zboží v přepravním kontejneru a cestě, a následně aktualizovat očekávané termíny dodání řádků nákupní objednávky. |
| Dotaz na náklady | <p>Otevře stránku **Dotaz na náklady**, která zobrazuje všechny náklady na cestu.</p><p>Po výběru možnosti **Zobrazit** v podokně akcí můžete upravit zobrazení. Můžete zobrazit kteroukoli z úrovní, plus kód položky a typu nákladů.</p><p>Na stránce **Poptávka nákladů** se zobrazí pouze ty kódy typů nákladů, které přímo souvisejí s transakcemi zásob. Odebráním těchto kódů typů nákladů můžete stránku upravit seskupením nákladů. Tato funkce může být užitečná, pokud používáte velikosti a barvy.</p><p>Stránka **Dotaz na náklady** zobrazuje pouze kódy typů nákladů, kde je pole **Debet** nastaveno na *Položka*.</p> |
| Objednávky přepravovaného zboží | Otevře stránku **Objednávky přepravovaného zboží**, která zobrazuje záznamy o přepravovaném zboží pouze pro vybranou cestu. |

## <a name="lines-view"></a>Zobrazení řádků

Chcete-li otevřít zobrazení **Řádky**, otevřete cestu a poté vyberte kartu **Řádky** v pravém horním rohu záhlaví cesty.

### <a name="information-on-the-voyage-header-fasttab"></a>Informace o záložce Záhlaví cesty

Záložka **Záhlaví cesty** v zobrazení **Řádky** cesty obsahuje základní informace, které cestu popisují. Mnoho polí, která se objevují na této záložce, se také objevují v zobrazení **Záhlaví**, jak je popsáno dále v tomto tématu.

### <a name="information-on-the-voyage-lines-fasttab"></a>Informace o záložce Řádky cesty

Záložka **Řádky cesty** v zobrazení **Řádky** cesty souvisí s podrobnostmi cesty a informacemi o kalkulaci nákladů, které platí na úrovni cesty. Zde si můžete prohlédnout přepravní kontejnery, folia a položky připojené k cestě. Zobrazuje se také cena a množství položek na cestě. Kliknutím na příslušný odkaz můžete zobrazit jakýkoli přepravní kontejner nebo folio, které je na seznamu.

### <a name="information-on-the-line-details-fasttab"></a>Informace na záložce Podrobnosti řádku

Záložka **Podrobnosti řádku** v zobrazení **Řádky** cesty ukazuje další informace o řádku, který je aktuálně vybrán na záložce **Řádky cesty**. Všimněte si, že tato záložka obsahuje podrobnosti o poloze, kterou každý řádek zaujímá v kontejneru, a jeho deklarované množství.

## <a name="header-view"></a>Zobrazení záhlaví

Chcete-li otevřít zobrazení **Záhlaví**, otevřete cestu a poté vyberte kartu **Záhlaví** v pravém horním rohu záhlaví cesty.

### <a name="settings-on-the-general-fasttab"></a>Nastavení na záložce Obecné

Následující tabulka popisuje pole, která jsou k dispozici na záložce **Obecné** zobrazení **Záhlaví** cesty.

| Pole | popis |
|---|---|
| Cesta | Zadejte číslo cesty nebo letu. |
| Odkaz na rezervaci | Pokud váš přepravce nebo přepravní středisko poskytuje referenční číslo pro identifikaci cesty (tj. interní referenci přepravce nebo přepravního střediska), zadejte jej sem. |
| Plavidlo | Zadejte nebo vyberte plavidlo. Pokud plavidlo není uvedeno jako hodnota, můžete zadat ID plavidla jako volný text. V takovém případě se hlavní tabulka neaktualizuje, aby bylo možné v tomto poli vybrat ID plavidla později. |
| Externí ID cesty | Zadejte veřejně dostupné ID pro cestu (například číslo letu). |
| Hlavní letecký nákladní list / přepravní doklad. | Zadejte hlavní letecký nákladní list nebo číslo přepravního dokladu. Tuto hodnotu můžete určit při letecké dopravě. |
| Letecký nákladní list / přepravní doklad | Pro přepravní kontejner zadejte domovský letecký nákladní list nebo přepravní doklad. |
| Vypůjčení | Zaškrtnutím tohoto políčka označíte, že kontejner je nájemním kontejnerem, který je třeba vrátit. |
| popis | Zadejte popis cesty, abyste ji snadněji rozpoznali. |
| Stav cesty | Stav cesty. Mezi hodnoty patří *Vytvořeno*, *Na cestě*, *Doklady přijaty*, a *Oceněno*. Toto pole není vypočítáno na základě logiky. Aktualizuje se pouze prostřednictvím akce účtování. Hodnota *Oceněno* označuje, že byla přijata faktura za sklad a všechny náklady na cestu. Pokud není faktura přijata, nemůže cesta dosáhnout stavu *Oceněno*. |
| Stav nákupní objednávky | Nejvyšší stav, kterého bylo dosaženo mezi všemi nákupními objednávkami spojenými s cestou. |
| Přijaté dokumenty | Hodnota, která označuje, zda vaše společnost obdržela všechny doklady spojené s cestou. Chcete-li změnit hodnotu, vyberte **Doklady přijaty** ve skupině **Aktualizace cesty** na kartě **Spravovat** v podoknu akcí. |
| Dopravní společnost | Pro tuto cestu vyberte přepravní společnost. Toto pole lze použít k určení automatických nákladů. |
| Jméno | Název společnosti, která je vybrána v poli **Přepravní společnost**. |
| Měrný systém | Toto pole umožňuje specifikovat měrný systém v automatických nákladech. Měrné systémy často používají organizace, které neznají individuální objem nebo hmotnost zboží, ale které vyžadují přesnější rozdělení, než jaké dovolují částky nebo množství. Spedice zajistí měření hmotnosti nebo objemu, a vy změřené údaje zapíšete na úrovni položky nebo nákupní objednávky. Může být automaticky aktualizováno, pokud je parametr vybrán nebo ho můžete zadat ručně. |
| Měrná jednotka | Měrná jednotka, která se vztahuje k číslu v poli **Měrný systém**. |
| Počet palet | Zadejte počet palet na řádku cesty. Toto pole se automaticky aktualizuje, pokud je možnost **Automaticky aktualizovat počet kartonů** nastavena na *Ano* na kartě **Obecné** stránky **Parametry nákladů za doručení**. |

### <a name="settings-on-the-delivery-fasttab"></a>Nastavení na záložce Dodání

Následující tabulka popisuje pole, která jsou k dispozici na záložce **Doručení** zobrazení **Záhlaví** cesty.

| Pole | popis |
|---|---|
| Datum a čas vytvoření | Datum a čas vytvoření záznamu cesty. |
| Datum expedice z továrny | Toto pole vybere nejstarší datum expedice z továrny mezi nákupními objednávkami, které jsou spojeny s cestou. Datum expedice z továrny je k dispozici v záhlaví nákupní objednávky a je aktualizováno pomocí funkce řízení sledování. |
| Datum expedice | Odhadované datum, kdy letadlo nebo plavidlo skutečně opustí výchozí místo cesty. |
| Datum odjezdu | Datum odjezdu je obvykle den, kdy letadlo nebo plavidlo skutečně opustí zámořský přístav. Datum expedice a datum odjezdu se nemusí shodovat. Pole **Datum odjezdu** slouží pouze pro informační účely. Nepoužívá se k odhadu očekávaného data dodání. Funkce řízení sledování se používá k odhadu očekávaného data dodání a toto pole lze nastavit tak, aby bylo automaticky vyplněno funkcí řízení sledování. |
| Datum uložení do skladu | Toto pole vybere nejdříve možné datum, kdy bude zboží z nákupních objednávek, které jsou spojeny s cestou, k dispozici k prodeji. |
| Odhadované datum doručení | Předpokládané datum dodání je obvykle datum, kdy má zboží dorazit do skladu. Toto pole je určeno pouze pro informaci. Nepoužívá se pro hlavní plánování zboží. Očekávané datum dodání na řádku nákupní objednávky se používá pro hlavní plánování zboží na cestě a je aktualizováno pomocí funkce řízení sledování. Toto pole lze nastavit tak, aby ho vyplnila funkce řízení sledování. |
| Skutečné datum dodání | Nejdřívější datum dodání, na základě zboží, které je spojeno s cestou. |
| Odhadovaný čas doručení do přístavu | Na základě informací, které vám poskytl přepravní agent, zadejte datum, kdy očekáváte, že cesta dorazí do přepravního přístavu. |
| Přijaté původní dokumenty | Zadejte datum přijetí původních dokladů. |
| Doporučeno zprostředkovatelem | Zadejte datum informování makléře. |
| Původní nákladní list odeslán | Zadejte datum, kdy byl odeslán původní nákladní list. |
| Uvolněné zboží | Zadejte datum, kdy bylo zboží propuštěno z celního úřadu. |
| Schůzka zákazníka | Zadejte datum schůzky se zákazníkem, což je datum, kdy očekáváte, že zákazník převezme vlastnictví zboží. |
| Doručeno na sklad | Zadejte datum, kdy bylo zboží doručeno do skladu. |
| Datum ověření | Zadejte datum ověření. |
| Instrukce k doručení | Zadejte datum přijetí pokynů pro doručení. |
| Způsob dodání | Toto pole poskytuje informace o metodě, která se používá k doručení cesty, a výběru nákladů na automatické náklady, které jsou spojeny s touto metodou doručení. |
| Výchozí přístav | Přepravní přístav, ze kterého cesta vychází. |
| Cílový přístav | Přepravní přístav, kam cesta dorazí. Přepravní kontejnery mohou mít jiné přístavy, protože loď se může zastavit ve více přístavech. Ověřením přístavu „do“ na úrovni přepravního kontejneru poskytnete přesné podrobnosti o přístavu pro každý přepravní kontejner na cestě. Automatické náklady spojené s přepravou se určují na základě kombinace typu přepravního kontejneru, přístavu „do“ a přístavu „od“. |
| Místní dopravce | Toto pole je určeno pouze pro informaci. Místní spedici by mělo být možné zvolit z tabulky dodavatele. |
| Datum místní přepravy | Datum, pro které je rezervována místní doprava. Toto pole může skladu pomoci s plánováním. |
| Čas místní přepravy | Časový úsek, pro který je rezervována místní doprava. Toto pole může skladu pomoci s plánováním. |
| Šablona cesty | Šablona cesty uvedená pro cestu. Šablona cesty se používá k zadání přístavu „do“ a přístavu „z“ přepravního kontejneru a plavby. Tyto hodnoty zase pomáhají identifikovat náklady na auto spojené s cestou. |

### <a name="settings-on-the-other-fasttab"></a>Nastavení na záložce Jiné

Následující tabulka popisuje pole, která jsou k dispozici na záložce **Jiné** zobrazení **Záhlaví** cesty.

| Pole | popis |
|---|---|
| Poznámky | Zadejte veškeré doplňující informace související s cestou. |
| Datum ocenění | Vyberte nejstarší datum expedice z továrny pro nákupní objednávky, které jsou spojeny s cestou. |
| Čekající cesta | Tímto způsobem můžete označit, zda vaše zásilka nebo cesta již odešla. Je určeno pouze pro informaci.  |
| Přejmenování přepravních kontejnerů | U cest, které mají více než jeden kontejner, počet kontejnerů, které ještě nebyly přijaty. |

## <a name="voyage-update-periodic-tasks"></a>Periodické úlohy aktualizace cesty

Modul **Náklady za doručení** obsahuje několik periodických úkolů souvisejících s cestou, které mohou hromadně aktualizovat několik aspektů cesty. Chcete-li tyto periodické úkoly spustit nebo naplánovat, přejděte na **Náklady za doručení \> Periodické úkoly \> Aktualizace cesty** a poté vyberte jeden z následujících typů úkolů:

- **Doklady přijaty** – Tento úkol vám umožní nastavit pole **Doklady přijaty** na *Ano* pro několik cest současně. Nastavení **Filtr** použijte k definování sady cest, které chcete aktualizovat.
- **Na cestě** – Tento úkol vám umožní nastavit **Stav cesty** na stav v přepravě, který je určen na stránce **[Parametry nákladů za doručení](landed-cost-parameters.md)**, pro několik cest současně. Nastavení **Filtr** použijte k definování sady cest, které chcete aktualizovat.
- **Připraveno k výpočtu nákladů** – Tento úkol vám umožní nastavit **Stav cesty** na stav Připraveno k výpočtu nákladů, který je určen na stránce **[Parametry nákladů za doručení](landed-cost-parameters.md)**, pro několik cest současně. Obvykle nastavíte tento úkol tak, aby běžel podle pravidelného plánu.
- **Oceněno** - Tento úkol vám umožní nastavit **Stav plavby** na stav Oceněno, který je stanoven na stránce **[Parametry nákladů za doručení](landed-cost-parameters.md)** pro několik cest současně, za předpokladu, že byly vypočteny náklady, ale dosud nebyly v cestě aktualizovány. Obvykle nastavíte tento úkol tak, aby běžel podle pravidelného plánu.
