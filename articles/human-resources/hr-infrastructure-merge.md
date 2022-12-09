---
title: Přehled sloučení infrastruktury Dynamics 365 Human Resources
description: Tento článek popisuje sloučení infrastruktury Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e68b28bfde35b51605aa0b653265da6261b69a90
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819235"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Často kladené dotazy ke sloučení infrastruktury Dynamics 365 Human Resources 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources poskytuje nástroje, které pomáhají personálním týmům zvýšit organizační agilitu, transformovat prostředí zaměstnanců a optimalizovat personální programy tak, aby se vytvořilo pracoviště, kde mohou lidé i firma prosperovat. Další informace o Dynamics 365 Human Resources viz [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformujte prostředí pro zaměstnance.** Udržte si špičkové výkony tím, že zmocníte manažery a zaměstnance prostřednictvím propojených samoobslužných prostředí, která podporují zapojení a růst.
- **Optimalizace personálních programů.** Pomozte snížit provozní náklady a vytvořte programy řízení dovolené a nepřítomnosti, času, benefitů a odměn zaměřené na lidi.
- **Zvýšení organizační agility.** Umožněte personálnímu oddělení pracovat s obratností, kterou firma vyžaduje, využitím Dataverse a Microsoft Power Platform k centralizaci dat o lidech a snadno rozšiřte Dynamics 365 Human Resources.
- **Objevte informace o pracovnících.** Rozhodujte se na základě dat prostřednictvím schopnosti analyzovat a vizualizovat data lidí na bohatých řídicích panelech, které jsou dostupné na jakémkoli zařízení.

## <a name="human-resources-infrastructure-merge"></a>Sloučení infrastruktury Human Resources

Dynamics 365 Human Resources je samostatná aplikace, která v současnosti využívá jinou infrastrukturu než ostatní finanční a provozní aplikace, například Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management. Sloučení infrastruktury přenese Dynamics 365 Human Resources do stejné infrastruktury jako ostatní finanční a provozní aplikace.

Chcete-li se dozvědět více o sloučení infrastruktury lidských zdrojů, viz [Časté otázky ke sloučení infrastruktury Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Odpovědi na často kladené otázky viz [Často kladené dotazy ke sloučení infrastruktury Human Resources](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Migrace zákazníků vs. sloučení zákazníků

V rámci sloučení infrastruktury byly všechny funkce aplikace Human Resources zpřístupněny v prostředí financí a provozu. Zákazníci mohou migrovat svá prostředí Human Resources pomocí nástrojů pro migraci, které jsou k dispozici v Microsoft Dynamics Lifecycle Services. Mohou také volitelně sloučit svá data se stávajícím finančním a provozním prostředím. 

Migrace a sloučení zákazníků se liší následujícím způsobem:

- **Migrace zákazníků** – Nástroj pro automatizovanou migraci se používá k provádění „migrace metodou lift-and-shift“ (přesun) zákaznické databáze z infrastruktury lidských zdrojů do infrastruktury financí a provozu. Výsledkem je nové finanční a provozní prostředí, které využívá databázi lidských zdrojů zákazníka. 
- **Sloučení zákazníků** – Microsoft tento dodatečný krok nevyžaduje. Děje se tak podle uvážení zákazníka a na jeho vlastní časové ose. V tomto kroku jsou data zákazníků přesunuta do stávajícího prostředí, například do prostředí Finance nebo Project Operations. Je to ruční proces a lze ho provádět pomocí datových entit rámce pro správu dat (DMF). 

## <a name="planning-a-human-resources-environment-migration"></a>Plánování migrace prostředí Human Resources

V rámci sloučení infrastruktury budou všichni zákazníci muset migrovat svá stávající prostředí Human Resources ze samostatné infrastruktury. Chcete-li tento proces usnadnit, doporučujeme použít nástroj pro automatickou migraci v Lifecycle Services k přesunu vašich aktuálních prostředí do nové infrastruktury. 

Následující části poskytují další podrobnosti o tom, jak používat nástroje Lifecycle Services k migraci samostatného prostředí Human Resources. 

Zákazníci, kteří plánují migraci, mohou mít následující očekávání:

- Všichni zákazníci budou muset před migrací svého provozního prostředí migrovat do sandboxového prostředí. 
- Nástroje pro migraci umožňují pouze migraci ze sandboxového do sandboxového prostředí a z provozního do provozního prostředí. Typ prostředí tedy určuje, jaké prostředí lze vhodně migrovat. 
- Zákazníci mohou před migrací svého provozního prostředí migrovat libovolný počet sandbxů, za předpokladu, že je k dispozici cílový slot sandboxu. Zákazníci také mohou migrovaný sandbox odstranit a opětovně migrovat vícekrát. 
- Pokud se migrace ze sandboxu nezdaří nebo pokud chcete začít znovu, můžete odstranit prostředí z finanční a provozní infrastruktury a znovu migrovat stejné prostředí.
- Adresa URL vašeho prostředí Human Resources se po migraci bude lišit.
- Naplánujte si přiměřené množství prostojů pro migraci vašeho provozního prostředí. Odhadovaný časový rámec pro dokončení procesu automatizované migrace jsou tři až čtyři hodiny. Časový rámec se bude lišit v závislosti na datech vaší organizace. Měli byste ověřit množství času, které je potřeba během migrace vašich sandboxových prostředí, a ponechat čas na jakékoli další ruční úlohy, které je třeba dokončit.

> [!IMPORTANT] 
> Když je provozní prostředí úspěšně migrováno do finanční a provozní infrastruktury, zdrojové samostatné provozní prostředí se automaticky odstraní. Migrované provozní prostředí byste neměli odstraňovat. 

Proces migrace je většinou automatický. Vaši firemní uživatelé však budou muset po migraci dokončit některé ruční kroky a ověření.

Musí být provedeny následující ruční kroky:

- Vytvořte nový projekt Lifecycle Services pro migraci.
- Upravte všechny integrace ve svém starém prostředí do nového prostředí nasměrováním integrace na nové adresy URL/koncové body na základě každé konfigurace integrace.
- Obnovte úložiště dat pro vložené sestavy Power BI.
- Obnovte seznam datových entit z pracovního prostoru DMF.
- Vyhledejte nápovědu v Lifecycle Services.
- Vytvořte fiskální kalendáře.

Během automatického procesu jsou dokončeny následující akce a měly by být ověřeny:

- Data:

    - Konfigurace
    - Role zabezpečení (včetně vlastních rolí)
    - Pracovní postupy (včetně oznámení)
    - Přizpůsobení a uložená zobrazení
    - Transakce
    - Vlastní pole
    - Přílohy
    - Výstrahy

- Správa dat - Použijte vlastní databázi (BYOD).
- Správa funkcí - povolené/zakázané funkce.
- Vložená aplikace Power Apps.
- Připojené prostředí centra pro správu Power Platform (pouze provozní).
- Dávkové úlohy.
- Pro každou právnickou osobu je vytvořena prázdná hlavní kniha. Pro každou hlavní knihu se nastaví výchozí typ kurzu a účetní měna.
- Automaticky se vytvoří nová účtová osnova a je propojena se stránkou **Hlavní kniha** v každé právnické osobě. Finanční dimenze, které jsou nakonfigurovány v prostředí Human Resources, budou automaticky přidány do nové struktury účtu a propojeny s hlavní knihou. 

> [!NOTE]
> Hlavní kniha je vyžadována pro finanční a provozní infrastrukturu jako součást produktu Dynamics 365 Finance. Řadič vlastní dimenze, který existoval v samostatné aplikaci Dynamics 365 Human Resources není k dispozici. Sloučená infrastruktura pro lidské zdroje závisí na finanční logice, aby se zobrazily finanční dimenze v modulu **Lidské zdroje**. Více informací o účtové osnově a finančních dimenzích získáte [tady](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Podmínky

- Migrace do prostředí bude vždy na nejnovější obecně dostupné (GA) verzi. V závislosti na vašem plánu migrace a testování, pokud vaše ověření migrace pro sandboxové prostředí bylo na jiné verzi, doporučujeme ověřit migraci sandboxu ve stejné verzi, jako je vaše provozní prostředí. 
- Během migrace budou migrovaná prostředí umístěna do stejné oblasti jako zdrojová samostatná prostředí lidských zdrojů.

## <a name="licensing"></a>Licence

V licencování nejsou žádné změny Dynamics 365 Human Resources v následujících oblastech: 

- **Minimální požadavky na zakoupení licence**
- **Licence na provozní prostředí a sandboxové prostředí** – Máte-li stávající samostatné licence pro lidské zdroje, které udělují jedno provozní prostředí a jedno sandboxové prostředí, bude stejný počet licencí k dispozici pro finanční a provozní infrastrukturu bez nákladů navíc.
- **Další licence sandboxu** – Pokud jste zakoupili další licence sandboxu pro samostatnou aplikaci Human Resources, stejný počet sandboxových licencí je k dispozici pro standardní akceptační testovací prostředí (sandbox) na finanční a provozní infrastruktuře, a to bez dalších nákladů. 
