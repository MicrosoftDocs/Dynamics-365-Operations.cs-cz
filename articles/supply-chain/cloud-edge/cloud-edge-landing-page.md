---
title: Jednotky škálování v distribuované hybridní topologii
description: Toto téma poskytuje informace o cloudových a hraničních jednotkách škálování pro pracovní zatížení výroby a správy skladu.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30f455f37b5161878cf9c864b92966aa74da051f
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376175"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>Jednotky škálování v distribuované hybridní topologii

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Schopnost jednotky škálování pro Microsoft Dynamics 365 Supply Chain Management je vám k dispozici za podmínek, kterými se řídí používání služby. Další informace naleznete v [právních informacích Microsoft Dynamics](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Povolením cloudových a hraničních jednotek škálování potvrzujete, že chápete, že některá data související s konfigurací a zpracováním cloudových a hraničních jednotek škálování mohou být uložena v datovém centru umístěném v USA. Chcete-li se dozvědět více o zpracování dat pro jednotky škálování cloudu a edge, podívejte se na [Zpracování dat během správy jednotek škálování](#data-processing-management) dále v tomto tématu.

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>Návrh základní hodnoty pro distribuovanou hybridní topologii

Společnosti, které pracují s výrobou a distribucí, musí být schopny provozovat klíčové obchodní procesy nepřetržitě, bez přerušení a v rámci škály. Distribuovaná hybridní topologie umožňuje společnostem bez přerušení spouštět zásadně důležité klíčové výrobní a skladové procesy, i když čelí příležitostným problémům s připojením k síti nebo latenci.

Distribuovaná hybridní topologie zavádí koncept *jednotky měřítka*, které umožňují distribuci zátěže výroby a skladu mezi různými prostředími. Tato funkce může pomoci zlepšit výkon, zabránit přerušení služeb a maximalizovat provozuschopnost. Jednotky škálování jsou poskytovány prostřednictvím následujících doplňků pro vaše předplatné Supply Chain Management:

- Doplněk cloudové jednotky škálování pro Dynamics 365 Supply Chain Management
- Doplněk hraniční jednotky škálování pro Dynamics 365 Supply Chain Management

Schopnosti pracovního zatížení jsou vydávány nepřetržitě prostřednictvím přírůstkových vylepšení.

## <a name="scale-units-and-dedicated-workloads"></a>Škálování jednotek a vyhrazená pracovní zatížení

Jednotky škálování rozšiřují vaše centrální prostředí centra Supply Chain Management přidáním vyhrazené kapacity zpracování. Jednotky škálování mohou běžet v cloudu. Alternativně mohou běžet v [hraniční síti](cloud-edge-edge-scale-units-lbd.md), onsite ve vašem místním zařízení.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 s jednotkami škálování.":::

Jednotky škálování poskytují odolnost, spolehlivost a škálování pro přiřazené úlohy. Jednotky škálování hrany lze dočasně odpojit od prostředí cloudového centra a pracovníci pokračují v práci v přiřazených úlohách na hraně.

*Úloha* je definovaná sada obchodních funkcí, kterou lze vyřadit a delegovat na jednotce škálování. Přestože byla uvolněna úloha pro správu skladu, úloha pro provádění výroby je stále v preview.

Můžete nakonfigurovat prostředí centra a jednotky škálování cloudu pro vybrané úlohy pomocí [portálu správce jednotky škálování](https://sum.dynamics.com). Můžete také přiřadit více úloh na jednotku škálování. Informace o předpokladech a omezeních pro jednotky škálování cloudu v aktuální verzi najdete v části [Předpoklady a omezení pro jednotky škálování cloudu](#cloud-scale-unit-prerequisites) dále v tomto tématu.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Možnosti úlohy vyhrazené správy skladu v jednotce škálování

Úlohy správy skladu umožňují škálovat vaše skladové operace a provozovat je v odolném prostředí pomocí izolovaných oken údržby. Úloha Warehouse Management podporuje většinu procesů Warehouse Management podnikového centra. Další informace naleznete v části [Pracovní zatížení pro jednotky škálování cloudu a hraniční sítě](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Funkce vyhrazeného pracovního vytížení v jednotce škálování

Výrobní úloha poskytuje následující možnosti:

- Obsluha strojů a vedoucí výroby mají přístup k operačnímu výrobnímu plánu.
- Operátoři strojů mohou udržovat aktuální plán spuštěním samostatných a procesních výrobních úloh.
- Vedoucí dílny může upravit operační plán.
- Pracovníci mají přístup k času a docházce pro označení příchodu a odchodu na hraně, aby zajistili správný výpočet platu pracovníka.

Další informace naleznete v části [Pracovní zatížení provádění výroby a jednotky škálování hrany](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Úvahy před aktivací distribuované hybridní topologie pro Supply Chain Management

Aktivací distribuované hybridní topologie převedete cloudové prostředí Supply Chain Management tak, aby fungovalo jako centrum. Můžete také přidružit další prostředí, která jsou nakonfigurována jako jednotky škálování v cloudu nebo na hraně.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Předpoklady a omezení pro cloudové jednotky škálování

V aktuální verzi pro jednotky škálování některé funkce ještě nejsou k dispozici, ale mohou být přidány v přírůstkových verzích v průběhu času.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Musíte být licencovaným zákazníkem Supply Chain Management

Chcete-li se připojit k distribuované topologii, musíte mít licenci pro Supply Chain Management. Vaše stávající cloudové prostředí se stane centrem vaší hybridní topologie. Prostředí sandbox i provozní prostředí můžete deklarovat jako prostředí centra a můžete přidat jednotky škálování podle doplňků, které získáte.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Váš stávající projekt musí být spravován prostřednictvím globální komerční verze LCS

Váš stávající projekt Microsoft Dynamics Lifecyle Services (LCS) musí splňovat následující požadavky na verzi:

- Projekt musí být spravován prostřednictvím globální komerční verze LCS na adrese [lcs.dynamics.com](https://lcs.dynamics.com).
- Místní verze LCS (např. [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) a [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) nejsou podporovány.
- Verze LCS pro vládní cloud nejsou podporovány.
- Verze LCS Mooncake není podporována.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Vaše aktuální produkční prostředí musí být v LCS samoobslužného typu

Vaše aktuální produkční prostředí musí být v LCS označeno jako **samoobslužného** typu. Tento typ označuje, že klient vašeho projektu LCS již byl převeden tak, aby podporoval model hostingu Azure Service Fabric.

> [!IMPORTANT]
> Typy prostředí, které běží jako infrastruktura jako služba (IaaS), nejsou podporovány. Tato prostředí jsou obvykle označena typem **Spravováno Microsoftem** v LCS. Pokud máte prostředí tohoto typu, pokuste se s kontaktem společnosti Microsoft porozumět vaší časové ose migrace na **samoobslužný** typ.

Microsoft je v procesu přechodu všech cloudových prostředí Supply Chain Management z modelu IaaS na topologii, která je hostována v Service Fabric. Tento krok přináší lepší škálovatelnost a usnadňuje správu služeb. Proto jsou operace nasazení a údržby rychlejší. Podobně komponenty služby migrují na koncept mikroslužeb a model hostování služby [přejde](/virtualization/windowscontainers/about/containers-vs-vm) z modelu virtuálního počítače (VM) do lehké kontejnerové architektury.

Nakonec bude stejná infrastruktura kontejnerových služeb založená na Service Fabric pohánět jak cloudové, tak hranové instance služby, bez ohledu na to, zda je instance centrum v cloudu nebo jednotka škálování v cloudu nebo na hraně.

Než se můžete připojit k hybridní topologii, která podporuje jednotky škálování, musí být váš klient projektu převeden na model hostovaný v Service Fabric. Kromě toho musí být převedeno jakékoli prostředí, které bude fungovat jako centrum.

> [!TIP]
> Chcete-li se informovat o stavu vašeho klienta projektu LCS, vyhledejte typ vašeho prostředí v [LCS](https://lcs.dynamics.com/) nebo se obraťte na svého partnera nebo kontaktujte společnost Microsoft.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Prostředí místních obchodních dat (místní) nejsou podporována jako centra pro jednotky škálování

Místní prostředí nemohou fungovat jako centra pro jednotky škálování. Prostředí centra musí být vždy hostovaná v cloudu.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Možnosti správy jednotek škálování jsou omezené

Možnosti správy, které mohou pomoci s přesunem úloh, jsou omezené. Některé operace správy nejsou podporovány samoobslužným způsobem a možná budete muset požádat o podporu prostřednictvím svého partnera nebo kontaktováním společnosti Microsoft. Mezi příklady patří některé pohyby úloh mezi jednotkami škálování a dočasné pohyby ad-hoc v situacích havárii.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Metriky a měření ještě nejsou k dispozici

Metriky a míry, které vám mohou pomoci vybrat nejlepší aplikaci pro vaše jednotky škálování, ještě nejsou k dispozici. Ve spolupráci s kontaktním nebo implementačním partnerem Microsoftu vyberte nejvhodnější aplikaci.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Zpracování dat během správy jednotek škálování

Když aktivujete prostředí Dynamics 365 na podporu distribuované hybridní topologie pro jednotky škálování cloudu a hrany, některé služby pro správu budou hostovány pouze ve Spojených státech, jako pro LCS. Toto chování ovlivňuje přenos a ukládání některých administrativních a konfiguračních informací, které používá [Portál správy jednotek škálování](https://sum.dynamics.com). Několik příkladů:

- Jména a ID klientů
- ID projektu LCS
- E-mailové adresy správce a vlastníka projektu, které se používají pro přihlášení
- ID prostředí pro jednotky centra a škálování
- Konfigurace úloh, včetně názvů a fyzických adres právnických osob a zařízení, aby mohla být vaše topologie zobrazena na geografické mapě
- Shromážděné metriky (například latence a propustnost), které se zobrazí na stránce analýzy mapy, vám pomohou vybrat nejpřínosnější využití vašich jednotek škálování

Data, která jsou přenesena do a uložena v datových centrech v USA, budou odstraněna podle zásad uchovávání dat společnosti Microsoft. Vaše soukromí je pro Microsoft důležité. Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Nasazení do distribuované, hybridní topologie pro Supply Chain Management

### <a name="try-out-the-distributed-hybrid-topology"></a>Vyzkoušení distribuované hybridní topologie

Proces zprovozňování distribuované hybridní topologie má dvě fáze. Během první fáze [vyzkoušejte](cloud-edge-try-out.md) řešení a ověřte svá přizpůsobení, abyste se ujistili, že fungují v distribuované topologii, která zahrnuje jednotky škálování. (K ověření můžete použít stávající vývojová prostředí.) Poté můžete pokračovat do druhé fáze, kde získáte produkční prostředí.

## <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>Výběr klienta projektu LCS a podrobný proces nasazení

Jednotky škálování jsou nabízeny ve více skladových jednotkách (SKU) a cenových možnostech. Proto si můžete vybrat možnost, která nejlépe odpovídá vašim plánovaným měsíčním objemům transakcí a výkonovým požadavkům.

> [!TIP]
> Chcete-li určit velikost, která nejlépe vyhovuje vašim potřebám, spolupracujte se svým implementačním partnerem a společností Microsoft, abyste porozuměli měsíční velikosti transakce, kterou požadujete.

Základní SKU se označuje jako *Základní* a výkonnější SKU se označuje jako *Standard*. Každá SKU je předem načtena s konkrétním počtem měsíčních transakcí. Můžete však zvýšit měsíční rozpočet transakcí přidáním nadbytečných doplňků pro každou SKU.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Doplňky cloudové jednotky škálování.":::

> [!NOTE]
> Doplňky škálovací jednotky nejsou spojeny s omezeným počtem uživatelů. Jsou dostupné všem uživatelům ve vašem stávajícím předplatném (za předpokladu, že jim váš administrátor přidělil požadované uživatelské role).

Nákup každého doplňku jednotky škálování vám nejen poskytne měsíční objem transakcí, ale také vás opravní k určitému počtu slotů prostředí v LCS. Za každý doplněk jednotky škálování cloudu máte nárok na jeden nový produkční slot a jeden nový slot sandbox. Během procesu registrace bude přidán nový projekt LCS, který má tyto sloty. Práva na použití pro sloty jsou vázána, takže sloty musí být použity jako jednotky škálování, které mají cloudové centrum.

Doplňky nadlimitního použití vás neopravňují k novým slotům prostředí.

Chcete-li získat více prostředí sandbox, můžete si zakoupit další běžné sloty sandbox. Microsoft vám pak může pomoci povolit tyto sloty jako jednotky škálování sandboxu pro hybridní topologii.


Poté, co dokončíte plánování, jak se připojíte k distribuované hybridní topologii pro řízení Supply Chain Management, použijete [Portál správy jednotky škálování](https://aka.ms/SCMSUM) k zahájení procesu registrace. V portálu vyberte kartu **Klienti Dynamics 365**. Tato karta zobrazuje seznam klientů, kterých je váš účet součástí a toho, kde jste vlastníkem nebo správcem prostředí pro projekt LCS.

Pokud klient, kterého hledáte, není v tomto seznamu, přejděte na [LCS](https://lcs.dynamics.com/v2) a ujistěte se, že jste buď správcem prostředí, nebo vlastníkem projektu LCS pro daného klienta. Pouze účty Azure Active Directory (Azure AD) od vybraného klienta mají oprávnění k dokončení registrace.

> [!NOTE]
> Poté, co použijete změny v LCS, může trvat až 30 minut, než se změny v seznamu klientů projeví.

U každého klienta se v seznamu zobrazuje stav zprovoznění.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Seznam klientů na kartě Dynamics 365.":::

Vyberte **Začněte kliknutím sem** k vyžádání zprovoznění pro klienta LCS. Musíte přijmout podmínky. Musíte také zadat pracovní e-mailovou adresu, na kterou může společnost Microsoft odesílat komunikaci související s procesem zprovoznění.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Předložení registrace klienta.":::

Microsoft zkontroluje váš požadavek a bude vás informovat o dalších krocích zasláním e-mailu na adresu, kterou jste uvedli v registračním formuláři. Microsoft bude s vámi úzce spolupracovat na aktivaci jednotek škálování v hybridní topologii pro váš obchodní scénář.

Po dokončení zprovoznění můžete port použít ke konfiguraci jednotek měřítka a úloh.

### <a name="manage-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Správa jednotek škálování a úkolů pomocí portálu správce jednotky škálování

Přejděte na [portál správce jednotky škálování](https://aka.ms/SCMSUM) a přihlaste se pomocí účtu klienta. Na stránce **Konfigurovat jednotky škálování** můžete přidat prostředí centra, pokud ještě není uvedeno. Poté můžete vybrat centrum, které chcete konfigurovat pomocí jednotek škálování a úloh.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Portál pro správu jednotek škálování, stránka Konfigurace jednotek škálování.":::

Chcete-li přidat jednu nebo více jednotek škálování, které jsou k dispozici ve vašem předplatném, vyberte **Přidat jednotky škálování**.

Na kartě **Definované úlohy** pomocí tlačítka **Vytvořit úlohu** přidejte správu skladu do některé z jednotek škálování. U každé úlohy musíte určit kontext procesů, které bude úloha vlastnit. Pro úlohy správy skladu je kontextem konkrétní sklad na konkrétním místě a právnické osobě.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Dialog Definice úloh.":::

#### <a name="manage-workloads"></a><a name="manage-workloads"></a>Správa úloh

Když je povolena jedna nebo více úloh, použijte možnost **Správa úloh**, chcete-li iniciovat a spravovat procesy, jako jsou ty, které jsou uvedeny v následující tabulce.

| Zpracovat | Popis |
|---|---|
| Pozastavte komunikaci s jednotkou škálování | Pozastavte zprávy kanálu mezi centrem a jednotkou škálování. Tento proces zastaví komunikaci a vyčerpá datový kanál mezi centrem a jednotkami škálování. Tento proces musíte spustit před spuštěním servisní operace Supply Chain Management buď v centru n ebo jednotce škálování, ale můžete jej použít i v jiných situacích. |
| Obnovte komunikaci s jednotkou škálování | Obnovte zprávy kanálu mezi centrem a jednotkou škálování. Tento proces může být nutné použít například poté, co spustíte servisní operaci Supply Chain Management v centru nebo jednotce škálování. |
| Upgrade úloh | Synchronizujte nové funkce mezi úlohami centra a škálovací jednotky. Tento proces může být nutné použít například tehdy, když servis způsobil změnu dotazů na výměnu dat a/nebo přidal k úloze nové tabulky nebo pole. |
| Přeneste úlohy na jednotku škálování | Naplánujte přesunutí úlohy, která aktuálně běží v centru, na jednotku škálování. Když je tento proces spuštěn, bude probíhat synchronizace dat a jak centrum, tak škálovací jednotka budou nastaveny tak, aby změnily vlastnictví úlohy. |
| Převeďte jednotku škálování na centrum | Naplánujte přesunutí úlohy, která aktuálně běží v jednotce škálování, na centrum. Když je tento proces spuštěn, bude probíhat synchronizace dat a jak centrum, tak škálovací jednotka budou nastaveny tak, aby změnily vlastnictví úlohy.
| Nouzový převod na centrum | <p>Okamžitě přeneste stávající úlohu do centra. *Tento proces změní vlastnictví pouze dat, která jsou aktuálně dostupná v centru.*</p><p><strong>Varování:</strong> Tento proces může způsobit ztrátu dat u nesynchronizovaných dat a selhání obchodního zpracování. Proto by se měl používat pouze v nouzových situacích, kdy musí být obchodní procesy zpracovány v centru, protože škálovací jednotka má výpadek, který nelze v přiměřené době zmírnit.</p> |
| Topologie distribuovaná vyřazením | Odstraňte nasazení škálovací jednotky a spusťte ji pouze v centru, bez zpracování úlohy. |

:::image type="content" source="media/sum-manage-workloads.png" alt-text="Zkušenosti se správou jednotky škálování a úlohy.":::

> [!TIP]
> Postupem času budou do prostředí správce jednotky škálování přidávána přírůstková vylepšení, která usnadní operace správy životního cyklu. Specifické funkce pro aktuální verzi jsou zdokumentovány v příručce pro zprovoznění, která je k dispozici zákazníkům, kteří jsou v procesu zprovoznění distribuované hybridní topologie pro Supply Chain Management. <!-- KFM: Add a link to the handbook when it is published -->

## <a name="feature-management-considerations-for-workloads"></a>Aspekty správy funkcí u úloh

Tato část vysvětluje některé důležité aspekty, které byste měli zvážit při instalaci úloh, přidávání funkcí nebo odebírání funkcí v nasazení distribuované hybridní topologie. Několik scénářů může ovlivnit to, zda budete muset spustit a [upgradovat úlohy](#manage-workloads) poté, co provedete změny. Obvykle to však budete muset udělat, když aktualizujete nebo přidáte nové dotazy na výměnu dat a/nebo když přidáte nové tabulky nebo pole do dříve nainstalované úlohy.

### <a name="mandatory-features-for-installing-a-workload"></a>Povinné funkce pro instalaci úlohy

Když nainstalujete úlohu, instalační proces vytvoří definici úlohy, která obsahuje informace o tabulkách dat, které se používají při synchronizaci dat mezi dvěma nasazeními. Vytvoření definice úlohy se automaticky zpracuje na základě funkcí, které jsou aktuálně povoleny ve [Správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). V následující tabulce jsou uvedeny funkce, které musejí být povoleny pro generování definic úloh, které jsou vyžadovány ke spuštění skladové nebo výrobní úlohy.

| Povinná funkce | Úloha |
|---|---|
| Automatické přiřazení GUID při vytváření uživatelů WHS | Sklad |
| Blokování práce pro celou organizaci | Sklad |
| Podrobnosti štítku vlny dodávky | Sklad |
| Podpora jednotek škálování pro seznamy prací skladové aplikace | Sklad |
| Provádění výrobního provozu | Výroba |

Když nasadíte pracovní zátěž pomocí [nástroje pro nasazení škálovatelných jednotek v samostatných vývojových prostředích](https://github.com/microsoft/SCMScaleUnitDevTools) nebo [portálu správce jednotek škálování](https://sum.dynamics.com), všechny povinné funkce budou automaticky povoleny. Pokud však provedete ruční testovací nasazení, ve kterém chybí jedna nebo více povinných funkcí, instalace úlohy se nezdaří a zobrazí se zpráva se seznamem chybějících funkcí. Poté musíte ručně povolit tyto funkce a znovu spustit instalaci úlohy.

### <a name="enabling-or-disabling-features-that-have-data-synchronization-dependencies"></a>Povolení nebo zakázání funkcí, které jsou závislé na synchronizaci dat

Funkce, které ovlivňují výběr dat synchronizovaných mezi centrem a jeho škálovacími jednotkami, také ovlivňují způsob vytvoření definice úlohy. Proto je důležité, aby byly tyto funkce povoleny před instalací úlohy. Pokud povolíte tento typ funkce, když je spuštěna úloha, musíte znovu vygenerovat definici úlohy spuštěním [upgradu úlohy](#manage-workloads) po aktivaci funkce. Podobně, pokud zakážete funkci, která má závislosti synchronizace dat, když spouštíte pracovní zátěž, musíte spustit [upgrade úlohy](#manage-workloads) k odstranění příslušných informací o synchronizaci dat z definice úlohy.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
