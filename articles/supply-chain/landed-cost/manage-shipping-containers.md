---
title: Správa přepravních kontejnerů
description: Tento článek popisuje, jak pracovat s přepravními kontejnery. Přepravní kontejnery se používají k seskupení zboží, které je seskupeno fyzicky. Používají se také v případech, kdy náklady musí být sdíleny pouze mezi tímto zbožím, obvykle proto, že jsou fyzicky pohromadě.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b409017407ce1c027184bdc2292197840c61e04a
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725434"
---
# <a name="manage-shipping-containers"></a>Správa přepravních kontejnerů

[!include [banner](../../includes/banner.md)]

Přepravní kontejnery se používají k seskupení zboží, které je seskupeno fyzicky. Používají se také v případech, kdy náklady musí být sdíleny pouze mezi tímto zbožím, obvykle proto, že jsou fyzicky pohromadě.

Chcete-li zobrazit a zpracovat zboží prostřednictvím stránky přepravního kontejneru, přejděte na **Náklady za doručení \> Přepravní kontejnery \> Všechny přepravní kontejnery**. Stránka **Všechny přepravní kontejnery** stránka zobrazuje seznam všech dostupných přepravních kontejnerů. Pomocí tlačítek v podoknu akcí můžete vytvářet či odstraňovat přepravní kontejnery a pracovat s nimi. Vyberte jakýkoli přepravní kontejner v seznamu a zobrazte jeho podrobnosti na stránce **Přepravní kontejnery**.

Horní část stránky s podrobnostmi přepravního kontejneru zobrazuje přepravní kontejner a informace o kalkulaci nákladů. V části **Řádky** jsou uvedena folia, položky a nákupní objednávky nebo převodní příkazy, které jsou připojeny ke kontejneru.

## <a name="action-pane"></a>Podokno akcí

Podokno akcí na stránkách **Všechny přepravní kontejnery** a **Přepravní kontejnery** poskytují tlačítka, která vám umožní pracovat s vybraným přepravním kontejnerem. Každé tlačítko provádí jednu akci. Podokno akcí také obsahuje karty, z nichž každá zase poskytuje sadu souvisejících tlačítek. Není-li uvedeno jinak, jsou všechna tlačítka a karty, které jsou popsány v následujících podsekcích, k dispozici jak v zobrazení seznamu (tj. na stránce **Všechny přepravní kontejnery**) a v podrobném zobrazení (tj. na stránce **Přepravní kontejnery**).

### <a name="buttons-on-the-manage-tab"></a>Tlačítka na kartě Správa

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na kartě **Spravovat** podokna akcí.

| Tlačítko | Popisy |
|---|---|
| Zaúčtovat příjemky | Zaúčtuje seznam příjemek nebo zobrazí seznamy příjemek produktů pro všechny řádky nákupní objednávky v přepravním kontejneru.  |
| Zaúčtovat příjemku produktu | Zaúčtuje příjemku produktu pro všechny řádky nákupní objednávky v přepravním kontejneru. |
| Zaúčtovat fakturu | Zaúčtuje fakturu pro všechny řádky nákupní objednávky v přepravním kontejneru.  |
| Převodní příkaz expedice | Zaúčtuje dodávku převodního příkazu pro všechny řádky nákupní objednávky v přepravním kontejneru. V dialogovém okně se zobrazí pouze ty řádky v přepravním kontejneru, které mají typ převodní příkaz. |
| Přijmout převodní příkaz | Zaúčtuje příjemku převodního příkazu pro všechny řádky nákupní objednávky v přepravním kontejneru. Dialogové okno pro příjem představuje nejjednodušší způsob přijímání zboží v přepravním kontejneru nebo cestě a je jednou ze tří dostupných možností. Můžete také přijímat prostřednictvím deníků doručení nebo zpracování na mobilním zařízení. |
| Vytvořit deník doručení | Deník doručení můžete generovat pro organizace pomocí pokročilých skladových funkcí. K dispozici jsou možnosti _Inicializovat množství_ (doporučeno) a buď _Vytvořit z přepravovaného zboží_, nebo _Vytvořit z nákupních objednávek_. Poslední dvě možnosti závisejí na tom, zda se používá zpracování přepravovaného zboží. |
| Přejmenovat | Otevře dialogové okno, kde můžete přejmenovat vybraný přepravní kontejner. |
| Změnit šablonu cesty | Změna šablony cesty. Po změně šablony cesty budete možná muset vybrat možnost **Najít automatické náklady** nebo znovu ručně přidat náklady, protože náklady na dopravu budou odstraněny. |
| Převést na pronájem | Převede vybraný přepravní kontejner na nájemní přepravní kontejner. |

### <a name="buttons-on-the-general-tab"></a>Tlačítka na kartě Obecné

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na kartě **Obecné** podokna akcí.

| Tlačítko | Popisy |
|---|---|
| Příjemka | Zaúčtuje seznam příjemek pro všechny řádky nákupní objednávky v přepravním kontejneru.  |
| Příjem produktu | Zobrazí záznam o příjemce produktu, pokud je použit. Proces přijetí produktu bude použit pouze v případě, kdy zboží nepoužívá funkci přepravovaného zboží. |
| Doručení položky | Zobrazí deník doručení zboží pro přepravní kontejner, pokud se tento deník používá. |
| Úseky | Úseky se používají k identifikaci samostatných částí cesty. Při sledování zásilky pomohou doby realizace, které lze přidružit ke každému úseku. Další informace najdete v tématu [Nastavení cesty s více úseky](multi-leg-journey-setup.md). |
| Sledování | Zobrazí nebo aktualizuje sledování dodávky. |
| Objednávky přepravovaného zboží | Stránku **Přepravované zboží** můžete otevřít přímo z kontejneru. Tato stránka zobrazuje záznamy o přepravovaném zboží pouze pro vybraný přepravní kontejner. |

## <a name="header-view"></a>Zobrazení záhlaví

Chcete-li otevřít zobrazení **Záhlaví**, otevřete přepravní kontejner a poté vyberte kartu **Záhlaví** v pravém horním rohu záhlaví přepravního kontejneru.

### <a name="settings-on-the-general-fasttab"></a>Nastavení na záložce Obecné

Následující tabulka popisuje nastavení, která jsou k dispozici na záložce **Obecné** zobrazení **Záhlaví** přepravního kontejneru.

| Pole | popis |
|---|---|
| Přepravní kontejner | Název přepravního kontejneru. |
| Cesta | Cesta, která je přiřazena k přepravnímu kontejneru. |
| Typ přepravního kontejneru | Zadejte typ přepravního kontejneru. Toto pole musí být nastaveno. Můžete jej použít k určení nákladů na přepravu, například výběrem automatických nákladů spojených s typem přepravního kontejneru. |
| Plavidlo | Zadejte nebo vyberte plavidlo. Pokud plavidlo není uvedeno jako hodnota, můžete zadat ID plavidla jako volný text. V takovém případě se hlavní tabulka neaktualizuje, aby bylo možné v tomto poli vybrat ID plavidla později. Další informace naleznete v tématu [Plavidla](shipping-information-setup.md#vessels). |
| Typ jednotky | Typy jednotek se používají jako další prostředek seskupování a identifikace přepravních kontejnerů. Jsou zobrazeny a vybrány na stránce přepravního kontejneru. Další informace naleznete v tématu [Nastavení typů jednotek](shipping-container-setup.md#unit-types). |
| Typ chlazení | Typy chlazení se používají jako další prostředek seskupování a identifikace přepravních kontejnerů, obvykle chladicích kontejnerů. Jsou zobrazeny a vybrány na stránce přepravního kontejneru. Další informace naleznete v tématu [Nastavení typů chlazení](shipping-container-setup.md#refrigeration-types). |
| Měrný systém | Toto pole umožňuje specifikovat měrný systém v modulu **Náklady za doručení**. Měrné systémy často používají organizace, které neznají individuální objem nebo hmotnost zboží, ale které vyžadují přesnější rozdělení, než jaké dovolují částky nebo množství. Spedice zajistí měření hmotnosti v kilogramech nebo objemu, a vy změřené údaje zapíšete na úrovni položky nebo nákupní objednávky. Může být automaticky aktualizováno, pokud je parametr vybrán nebo ho můžete zadat ručně. |
| Měrná jednotka | Měrná jednotka, která se vztahuje k číslu v poli **Měrný systém**. |
| Skutečná hmotnost | Můžete zaznamenat skutečnou hmotnost kartonu nebo kontejneru. Tuto hodnotu lze použít k ověření proti maximální hmotnosti povolené v nastavení přepravního kontejneru. |
| Počet kartonů | Pokud je vybrán parametr, počet kartonů se automaticky aktualizuje. |
| Popis zboží | Popis zboží lze vybrat na přepravním kontejneru nebo záhlaví folia. Používá se k identifikaci cesty, přepravního kontejneru nebo folia zboží. Více informací naleznete v tématu [Popis zboží](shipping-information-setup.md#description-of-goods). |
| Letecký nákladní list / přepravní doklad | Pro přepravní kontejner můžete zadat domovský letecký nákladní list nebo přepravní doklad. |
| Poznámky | Doplňující informace související s přepravním kontejnerem. |
| Vratný | Hodnota, která označuje, zda lze přepravní kontejner po cestě vrátit. |
| Stav cesty | Stav cesty, který je přiřazen přepravnímu kontejneru. |
| Stav nákupní objednávky | Stav nákupní objednávky, který je přiřazen přepravnímu kontejneru. |

### <a name="settings-on-the-delivery-fasttab"></a>Nastavení na záložce Dodání

Následující tabulka popisuje nastavení, která jsou k dispozici na záložce **Doručení** zobrazení **Záhlaví** přepravního kontejneru.

| Pole | popis |
|---|---|
| Datum a čas vytvoření | Datum a čas vytvoření přepravního kontejneru. |
| Datum expedice z továrny | Toto datum je obvykle poskytováno továrně / dodavateli k označení, kdy očekáváte, že zboží opustí své místo. Když pracujete s továrnou v Asii, je často vyžadováno toto datum místo data, do kterého očekáváte zboží. (Naproti tomu u místního doručení je požadováno datum, do kterého očekáváte zboží.) Toto pole lze vyplnit z řádků nákupní objednávky v seznamu přepravních kontejnerů. Můžete ho také zadat ručně zde. |
| Datum expedice | Toto datum lze vytisknout na dokladu nákupní objednávky. Obvykle informuje továrnu / dodavatele o datu, do kterého by mělo být zboží doručeno do přístavu. Toto pole je určeno pouze pro informaci. Nepoužívá se k odhadu očekávaného data doručení zboží v přepravním kontejneru. Toto pole lze nastavit tak, aby se automaticky aktualizovalo při aktualizaci stránky řízení sledování. |
| Datum uložení do skladu | Nejdříve možné datum, kdy bude zboží z nákupních objednávek, které jsou spojeny s cestou, k dispozici k prodeji.|
| Odhadované datum doručení | Obvykle datum, kdy má zboží dorazit do skladu. Toto pole je určeno pouze pro informaci. Nepoužívá se k výpočtu hlavního plánování na řádcích nákupní objednávky v přepravním kontejneru. Očekávané datum doručení na řádcích nákupní objednávky je aktualizováno prostřednictvím řízení sledování. Toto pole lze nastavit tak, aby se aktualizovalo při aktualizaci stránky řízení sledování. |
| Datum odjezdu | Obvykle datum, kdy letadlo nebo plavidlo skutečně opustí zámořský přístav. |
| Odhadovaný čas doručení do přístavu | Odhadovaný den příjezdu do cílového přístavu (přístav „do“). |
| Přijaté původní dokumenty | Volitelné: Aktualizujte datum přijetí původních dokladů. |
| Doporučeno zprostředkovatelem | Volitelné: Aktualizujte datum informování makléře. |
| Původní nákladní list odeslán | Volitelné: Aktualizujte datum, kdy byl odeslán původní nákladní list. |
| Uvolněné zboží | Volitelné: Aktualizujte datum uvolnění zboží. |
| Schůzka zákazníka | Volitelné: Aktualizujte datum schůzky se zákazníkem. |
| Doručeno na sklad | Volitelné: Aktualizujte datum, kdy bylo zboží doručeno do skladu. |
| Datum ověření | Volitelné: Aktualizujte datum ověření. |
| Instrukce k doručení | Volitelné: Aktualizujte datum pokynů k doručení. |
| Výchozí přístav | Přístav, ze kterého budou položky odeslány. |
| Cílový přístav | Přístav, do kterého budou položky odeslány. |
| Místní dopravce | Toto pole je určeno pouze pro informaci. Místní spedici by mělo být možné zvolit z tabulky dodavatele. |
| Datum místní přepravy | Zadejte datum, pro které je místní doprava rezervována. Toto pole může skladu pomoci s plánováním. |
| Čas místní přepravy | Zadejte časový úsek. Toto pole může skladu pomoci s plánováním. |
| Šablona cesty | Šablona cesty uvedená pro cestu. Šablona cesty poskytuje podrobnosti o přístavech „do“ a „od“ a doby realizace, které jsou spojeny s řízením sledování přepravního kontejneru. |

### <a name="settings-on-the-other-fasttab"></a>Nastavení na záložce Jiné

Následující tabulka popisuje nastavení, která jsou k dispozici na záložce **Jiné** zobrazení **Záhlaví** přepravního kontejneru.

| Pole | popis |
|---|---|
| Vypůjčení | Hodnota, která označuje, zda je přepravní kontejner nájemním přepravním kontejnerem. Náklady na pronájem mohou být přidruženy nájemním kontejnerům. |
| Převedeno na pronájem | Hodnota, která označuje, zda byl přepravní kontejner převeden na nájemní přepravní kontejner. Náklady na pronájem mohou být přidruženy nájemním kontejnerům. |
| Původní cesta | Pokud byl přepravní kontejner přesunut na novou cestu, původní cesta. |
| Použito | Toto pole použijte k zaznamenání, zda byl použit nájemní přepravní kontejner. Je určeno pouze pro informaci. |
| Očekávané datum naložení | Datum, kdy se očekává naložení zboží do přepravního kontejneru. |
| Naše sériové číslo | Zadejte sériové číslo, které vaše společnost interně používá pro přepravní kontejner. |
| Sériové číslo přepravní společnosti | Zadejte sériové číslo, které pro přepravní kontejner poskytla přepravní společnost nebo agent. |
| Datum uplatnění osvědčení o zkoušce | Datum, kdy byla požadována zkouška přepravního kontejneru. |
| Datum přijetí osvědčení o zkoušce | Datum přijetí osvědčení o zkoušce. |
| Datum vypršení osvědčení o zkoušce | Datum vypršení platnosti osvědčení o zkoušce. |
| Číslo osvědčení o zkoušce | Číslo certifikátu, který byl vydán po provedení zkoušky. |

## <a name="lines-view"></a>Zobrazení řádků

Chcete-li otevřít zobrazení **Řádky**, otevřete přepravní kontejner a poté vyberte kartu **Řádky** v pravém horním rohu záhlaví přepravního kontejneru.

### <a name="information-on-the-shipping-container-fasttab"></a>Informace na záložce Přepravní kontejner

Záložka **Přepravní kontejner** v zobrazení **Řádky** zobrazuje informace o přepravním kontejneru. Většina z těchto informací se také objevuje v zobrazení **Záhlaví**, jak je popsáno výše v tomto článku.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informace a tlačítka na záložce Řádky

Záložka **Řádky** v zobrazení **Řádky** ukazuje podrobnosti o každém úplném nebo částečném řádku nákupní objednávky, který je zahrnut v aktuálním přepravním kontejneru.

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na záložce **Řádky** v zobrazení **Řádky**.

| Tlačítko | popis |
|---|---|
| Odebrat | Odebere z cesty vybraný řádek nákupní objednávky. |
| Zásoby \> Transakce | Zobrazí transakce zásob pro vybraný řádek nákupní objednávky. Pokud používáte přepravované zboží, zobrazí se také původní objednávka a objednávky přepravovaného zboží. |
| Zásoby \> Zobrazit dimenze | Otevře dialogové okno, kde můžete vybrat dimenze zásob pro zobrazené transakce. |
| Znovu načíst | Aktualizuje informace, které souvisejí s množstvím, hmotností nebo objemem vybraného řádku nákupní objednávky. |

### <a name="information-on-the-lines-details-fasttab"></a>Informace na záložce Podrobnosti řádků

Záložka **Podrobnosti řádků** v zobrazení **Řádky** ukazuje podrobnosti o řádku nákupní objednávky, který je aktuálně vybrán na záložce **Řádky**.
