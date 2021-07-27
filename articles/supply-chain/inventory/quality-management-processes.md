---
title: Přehled správy kvality a neshod
description: Toto téma představuje funkce správy kvality a neshod v Microsoft Dynamics 365 Supply Chain Management a vysvětluje, jak mohou pomoci zlepšit kvalitu produktů ve vašem dodavatelském řetězci.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11574"
- intro-internal
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8bb3862b2a082dd975af8bbb30961caf209c5ad
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344513"
---
# <a name="quality-and-nonconformance-management-overview"></a>Přehled správy kvality a neshod

[!include [banner](../includes/banner.md)]

Toto téma představuje funkce správy kvality a neshod v Microsoft Dynamics 365 Supply Chain Management a vysvětluje, jak mohou pomoci zlepšit kvalitu produktů ve vašem dodavatelském řetězci.

Zajištění kvality zahrnuje testování produktů a správu nevyhovujícího materiálu. Procesy řízení kvality pomáhají zajistit vysokou úroveň kvality produktu ve vašem dodavatelském řetězci. Tyto procesy také pomáhají optimalizovat procesy dodavatelského řetězce a zvýšit spokojenost zákazníků. Správa kvality pomáhá se správou doby oběhu objednávky při zpracování nevyhovujících produktů bez ohledu na místo jejich původu. Výsledky diagnostiky propojit s úlohami oprav. V systému můžete naplánovat úlohy k nápravě problémů a zabránit tak opakování těchto problémů v budoucnosti. Řízení kvality také umožňuje sledování problémů (včetně interních) podle typu problému a umožňuje určit krátkodobé nebo dlouhodobé řešení. Statistické údaje o klíčových ukazatelích výkonu (KPI) nabízí náhled na potíže s neshodami, které se dříve objevily, a řešení, která byla použita k jejich nápravě. Historická data můžete použít ke kontrole účinnosti předchozích opatření pro zajištění kvality a k rozhodnutí o tom, zda tato opatření použít i v budoucnu.

Správa kvality pomáhá se správou doby oběhu objednávky při zpracování nevyhovujících produktů bez ohledu na místo jejich původu. Vzhledem k tomu, že typy diagnostiky jsou propojeny s vykazováním oprav, aplikace Supply Chain Management může naplánovat úlohy pro nápravu problémů a zabránění jejich opakování.

Kromě funkcí pro správu neshod obsahuje moduly správy kvality také funkce pro sledování problémů podle jejich typu (i když jsou interní potíží) a pro určování krátkodobých a dlouhodobých řešení. Statistické údaje o klíčových ukazatelů výkonnosti (KPI) nabízí náhled na historii předchozích potíží s neshodami a řešení, která byla použita k jejich nápravě. Historická data můžete použít ke kontrole účinnosti předchozích opatření pro zajištění kvality a k rozhodnutí o tom, zda tato opatření použít i v budoucnu.

Při nastavování přidružení kvality může aplikace Supply Chain Management vygenerovat objednávky kvality pro různé obchodní procesy, události a podmínky. Přiřazení kvality může zahrnovat určitou položku, určitou skupinu položek nebo všechny položky.

## <a name="examples-of-the-use-of-quality-management"></a>Příklady použití správy kvality

Správa kvality je flexibilní a lze ji implementovat různými způsoby, aby byly splněny požadavky konkrétních úrovní operací dodavatelsko-odběratelského řetězce. V následujících příkladech jsou znázorněna možná použití těchto funkcí:

- Automatické spuštění procesu řízení kvality na základě předem definovaných kritérií (například při registraci nákupní objednávky od konkrétního dodavatele ve skladu).
- Blokování zásob při inventuře zabraňuje použití neschválených zásob (úplné blokování množství nákupní objednávky).
- Použití vzorkování jako součásti přidružení k definici množství aktuálních fyzických zásob, které je nutné zkontrolovat. Vzorkování může být založeno na pevném množství, procentuální hodnotě nebo celé licenční značky.
- Vytvořte objednávky kvality pro částečné příjmy. Abyste mohli vytvořit objednávku kvality, která je založena na množství fyzicky přijatém s objednávkou, je nutné zaškrtnout políčko **Na aktualizované množství** na stránce **Vzorkování položky**.
- Vytvoření typů testu, které zahrnují minimální, maximální a cílové hodnoty testu, a vykonání testu kvality vůči množství s předdefinovanými ověřovacími výsledky.
- Určení přijatelné úrovně kvality (AQL) pro řízení odchylek měření kvality.
- Určení zdrojů vyžadovaných operací kontroly, jako je například prostor testu nebo testovací přístroje.

> [!NOTE]
> Funkce _Správa kvality pro procesy skladu_ rozšiřuje možnosti správy kvality. Používáte-li tuto funkci, přejděte do tématu [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md), kde najdete příklady, jak povolit správu kvality.

## <a name="controlling-the-quality-management-process"></a>Řízení procesu správy kvality

Zde je několik způsobů, jak řídit proces správy kvality:

- Vytvořte objednávku kvality, která bude založena na aktivačních bodech, jako je například "příjemka produktu" u příchozích operací nebo "při vydání produktu" pro odchozí operace.
- Zdokumentujte výsledky testů a zjistěte, zda výsledky odpovídají stanoveným kritériím testování a přijatelným úrovním kvality.
- Použijte správu dokumentů pro podrobné specifikace produktu a uživatelské poznámky v rámci vykazování během procesu kontroly.
- Uchovejte nevyhovující produkty a porovnejte je s dalšími informacemi o neshodách, aby bylo možné zjistit původní příčinu problému.
- Zdokumentujte náklady na správu neshod. Tyto náklady zahrnují zboží (například náhradní díly), vedlejší náklady a časové výkazy s počtem pracovních hodin vyžadovaných k opravě neshody.
- Naplánujte procesy opravy chyby pomocí zpracování opravy, která je propojena s objednávkou kvality.

[![Proces správy kvality.](media/quality-management-process-diagram.png)](media/quality-management-process-diagram.png)

## <a name="product-testing-and-quality-orders"></a>Testování produktů a objednávky kvality

Testování výrobků se obvykle nazývá kontrola kvality a používá objednávky kvality. Pomocí funkce kontroly kvality můžete provést následující:

- Definujte testy, které je třeba u materiálu provádět. Tyto testy zahrnují specifikace kvality, použitý testovací přístroj, dokumenty popisující testování, plán vzorkování a přijatelné úrovně kvality.
- Vytvořte objednávku kvality, která určuje, jaké testy musí být provedeny pro určitou objednávku, například nákupní nebo výrobní zakázku, nebo pro určité množství zásob. Objednávku kvality můžete vytvořit ručně nebo ji můžete generovat automaticky podle pokynů týkajících se kvality.
- Definujte pokyny týkající se kvality spojené s nákupními objednávkami, karanténními příkazy, výrobními zakázkami nebo prodejními objednávkami v jednotlivých obchodních postupech, pro automatické generování objednávky kvality, která definuje požadavky na zkoušky příchozího nebo odchozího materiálu.
- Zaznamenejte výsledky testů v objednávce kvality, ověřujte výsledky testů s přijatelnou úrovní kvality a tiskněte certifikát analýzy s výsledky testů.

## <a name="nonconformance"></a>Neshoda

Neshoda popisuje položku, která má potíže s kvalitou. Proces neshody umožňuje vytvořit objednávku neshody, která popisuje množství nevyhovujícího materiálu, příčinu a typ problému a vysvětlující komentáře. Předdefinováním klasifikace typu problémů můžete usnadnit analýzu nevyhovujícího materiálu. Lze také vytisknout značku neshody a sestavu neshody s cílem řídit likvidaci nevyhovujícího materiálu. Značka a sestava může například značit podmínku **Nepoužitelné** nebo **Omezené použití**.

V následující tabulce je uvedeno šest výchozích typů neshod a popis informací, které musí být zaznamenány pro jednotlivé typy.

| Typ neshody | Informace o zdroji |
|---|---|
| Odběratel | Číslo účtu odběratele, číslo prodejní objednávky nebo číslo šarže pro transakci prodejní objednávky. Neshoda může například souviset s určitou dodávkou prodejní objednávky nebo se zpětnou vazbou odběratele ohledně kvality výrobku. |
| Požadavek na službu | Číslo účtu odběratele, číslo prodejní objednávky nebo číslo šarže pro transakci prodejní objednávky. Neshoda může například souviset s určitou dodávkou prodejní objednávky nebo se stížností odběratele na kvalitu položky. |
| Dodavatel | Číslo účtu dodavatele, číslo nákupní objednávky nebo číslo šarže pro transakci nákupní objednávky. Neshoda může například souviset s příjmem nákupní objednávky nebo s otázkami dodavatele ohledně součásti, kterou dodává. |
| Výroba | Číslo výrobní zakázky nebo číslo šarže pro transakci výrobní zakázky. Neshoda může například souviset s určitou vyrobenou dávkou. |
| Interní | Číslo objednávky kvality nebo číslo šarže kvality pro transakci objednávky kvality. Neshoda může například souviset s testy, které jsou provedeny v rámci objednávky kvality nebo s otázkami zaměstnance ohledně kvality výrobku. |
| Výroba vedlejších produktů | Neshoda výrobní zakázky na vedlejší produkt, která souvisí s dávkovými výrobními zakázkami. |

Neshody jsou přidruženy k typu problému. Typy problémů jsou definovány na stránce **Typy problémů**, kde můžete určit, jaké typy problémů lze přiřadit ke každému typu neshody. Například typy problémů pro neshody typu **Servisní požadavek** mohou odrážet klasifikaci stížností odběratelů, zatímco typy problémů pro neshody typu **Interní** mohou představovat klasifikaci kódů defektů.

Při vytvoření nové neshody vyberte typ neshody a typ problému. Počáteční stav schválení je **Nový** a představuje požadavek na akci. Následujícím krokem je změna stavu schválení na **Schváleno** nebo **Odmítnuto**, který značí, že provedete nebo neprovedete akci pro neshody. Neshodu lze také uzavřít (zaškrtnutím samostatného políčka), čímž označíte, že jste ji dokončili, nebo můžete neshodu znovu otevřít, čímž označíte, že je nutné další zvážení.

Můžete zadat komentáře pro neshodu připojením dokumentu. Je vhodné definovat jedinečný typ dokumentu pro neshody pomocí stránky **Typ dokumentu**. Poté můžete pomocí stránky **Nastavení sestavy** definovat, zda mají být komentáře pro tento typ dokumentu vytištěny v sestavě neshody a na značce neshody. Sestavu a značku neshody lze použít k uspořádání podkladů. Sestavy a značky lze výběrově generovat na základě kritérií výběru, která jsou přidružena s danou neshodou. Tato kritéria zahrnují číslo neshody, zboží, odběratele, dodavatele a stav.

Sestava neshody zobrazuje číslo neshody, zboží a typ problému. V závislosti na zásadách nastavení sestavy může sestava obsahovat také související poznámky k neshodě. Značka neshody zobrazuje podobné informace a také obsahuje karanténní zónu a typ (například **Omezené použití** nebo **Nepoužitelné**), který jste přiřadili neshodě za účelem likvidace vadného materiálu.

## <a name="approved-nonconformance"></a>Potvrzená neshoda

Pro schválenou neshodu lze nepovinně definovat alespoň jednu související operaci. Související operace popisuje očekávanou práci, která má být provedena, a obsahuje seznam operací kvality, které jste definovali, a popisný text o důvodu dané práce. Po definici operace můžete nepovinně definovat vedlejší náklady, položky a časové rozpisy odpracovaných hodin, které jsou zapotřebí pro provedení práce. Vypočtené náklady jsou zobrazeny pro související informace a pro neshody se zobrazují celkové vypočtené náklady. Vypočtené náklady a podkladové podrobnosti (o položkách, odpracovaných hodinách a vedlejších nákladech) představují referenční informace, které se používají pouze ve funkci pro správu kvality.

Objednávku kvality můžete volitelně vytvořit z neshody nejprve provedením dotazu na objednávky kvality a následným vytvořením nové objednávky kvality. Objednávka kvality může například identifikovat potřebu otestovat (nebo přetestovat) vadný materiál. Nově vytvořená objednávka kvality zobrazuje odkaz na původní neshodu.

Nepovinně lze propojit jednu neshodu k jiné a vytvořit ze stávající neshody novou neshodu. Propojení může například označovat vzájemnou souvislost mezi problémy s kvalitou.

## <a name="correction-handling"></a>Zpracování opravy

Stránka **Opravy** umožňuje vytvořit seznam neshod, které musí být opraveny. Každá položka opravy je přidružena typu diagnostiky, který způsobil problém, který má být zjištěn. Stránka **Opravy** také obsahuje informace o tom, kdo musí provést nápravná opatření a kdy. Můžete popsat podrobnosti o problému a nápravná opatření, která požaduje připojení dokumentu k opravě. Poté, co byla neshoda vyřešena nebo opravena, "uzavřete" položku opravy výběrem možnosti **Dokončeno**. Lze rovněž určit, že řešení bylo krátkodobé.

Je vhodné definovat jedinečný typ dokumentu pro opravy pomocí stránky **Typ dokumentu**. Poté můžete pomocí stránky **Nastavení sestavy** definovat, zda mají být komentáře pro tento typ dokumentu vytištěny v sestavě opravy. Vytištěná sestava opravy zobrazuje informace o neshodě a související poznámky k neshodě. Sestava také obsahuje informace o opravě, například typ diagnostiky a související poznámky k opravě.

## <a name="additional-resources"></a>Další prostředky

- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Blokování zásob](inventory-blocking.md)
- [Karanténní příkazy](quarantine-orders.md)
- [Kontrola kvality zboží](tasks/inspect-quality-goods.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
