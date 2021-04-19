---
title: Cloudové jednotky a hraniční jednotky škálování pro pracovní zatížení výroby a správy skladů
description: Toto téma poskytuje informace o cloudových a hraničních jednotkách škálování pro pracovní zatížení výroby a správy skladu.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3eacc9d0cf53fa8af3ff166006cb8fab32445331
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836703"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Cloudové jednotky a hraniční jednotky škálování pro pracovní zatížení výroby a správy skladů

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Jednotky v cloudu a hraniční jednotky škálování umožňují distribuci pracovních zátěží v dílně a ve skladech mezi různými prostředími. Tato funkce může pomoci zlepšit výkon, zabránit přerušení služeb a maximalizovat provozuschopnost. Zajišťují je následující doplňky:

- Doplněk cloudové jednotky škálování pro Dynamics 365 Supply Chain Management
- Doplněk hraniční jednotky škálování pro Dynamics 365 Supply Chain Management

Společnosti, které pracují s výrobou a distribucí, musí být schopny provozovat klíčové obchodní procesy nepřetržitě, bez přerušení a v rámci škály. Cloudové a hraniční jednotky škálování umožňují společnostem bez přerušení spouštět zásadně důležité klíčové výrobní a skladové procesy, i když čelí příležitostným problémům s připojením k síti nebo latenci.

## <a name="public-preview-information"></a>Informace Public Preview

Náhled poskytuje jedno prostředí, které funguje jako cloudové centrum vašeho prostředí Dynamics 365 Supply Chain Management a jedno prostředí, které funguje jako cloudová jednotka škálování.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Náhled dostupnosti

Náhled pro cloudové a hraniční jednotky škálování bude pro stávající zákazníky Supply Chain Management k dispozici v říjnu 2020.

Přístup k říjnové verzi Preview 10.0.15 / aktualizace platformy 39 pro nasazení ve vašem prostředí [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2), musíte být součástí náhledu programu vdčasného přístupu (známého také jako PEAP) pro Supply Chain Management. Pokud jste již členem širšího [Dynamics Insider Program](https://experience.dynamics.com/insider), můžete se připojit k PEAP. Stačí vybrat konkrétní program s názvem „Finance & Operations: Preview early access program (PEAP).“

> [!IMPORTANT]
> Schopnost jednotky škálování pro Supply Chain Management je k dispozici, pouze pokud souhlasíte s [podmínkami Cloud + Edge Preview pro Finance and Operations](https://Aka.ms/SCMCnETerms).

### <a name="data-processing-for-the-preview"></a>Zpracování dat pro náhled

Během verze public preview budou některé služby správy hostovány pouze ve Spojených státech. Když se však funkce stane obecně dostupnou, budou tyto služby správy k dispozici ve všech zemědělských oblastech podporovaných Supply Chain Management. To ovlivní přenos a ukládání administrativních informací používaných správcem jednotek škálování, včetně:

- Jména a ID klientů
- ID projektu LCS
- E-maily správce používané k přihlášení
- ID prostředí pro jednotky centra a škálování
- Konfigurace úloh
- Shromážděné metriky (například latence a propustnost), které se zobrazují na stránce analýzy mapy

Data přenesená do datových center v USA a uložená v nich budou po ukončení prostředí náhledu odstraněna.

### <a name="sign-up-for-the-preview"></a>Registrace náhledu

Chcete-li se zaregistrovat do cloudového a hraničního náhledu pro Supply Chain Management, vaše organizace musí mít živé cloudové prostředí Supply Chain Management.

Možnosti jednotky škálování jsou aktuálně ve verzi public preview. Při registraci musíte použít uživatelský účet u konkrétního klienta. Musíte být také vlastníkem projektu nebo správcem prostředí v LCS pro aktivní projekt Dynamics 365 LCS v daném klientovi.

Když se zaregistrujete k náhledu, vyberete klienta a projdete kroky registrace. Jakmile může společnost Microsoft přidělit kapacitu náhledu, pošleme vám e-mail, který obsahuje podrobnosti o zřízení a propagační (promo) kódy pro dvě prostředí (centrum a jednotka škálování) pro příslušný projekt LCS. Poté budete moci nasadit obě prostředí jako prostředí sandbox úrovně 2. Tato prostředí budou platná 60 dní od data vytvoření promo kódů. Tato dvě prostředí byste neměli používat, dokud nebude dokončen krok popsaný v následujícím odstavci.

Poté, co společnosti Microsoft potvrdíte, že tato dvě prostředí byla nasazena pomocí promo kódů, bude jedno z prostředí nakonfigurováno tak, aby fungovalo jako centrum, a druhé bude nakonfigurováno tak, aby fungovalo jako jednotka škálování. Potom můžete nakonfigurovat jednotky škálování a nasadit vybrané úlohy správy skladu a výroby pomocí [portálu pro správu jednotek škálování](https://aka.ms/SCMSUM).

Prostředí náhledu budou automaticky odstraněna po 60 dnech. Mohou však být odstraněny dříve, pokud se ukáže, že se nepoužívají. Po odstranění prostředí náhledu se můžete zaregistrovat a zařadit do fronty nové nasazení náhledu.

Chcete-li se přihlásit k náhledu, přejděte na [Portál správce jednotky škálování](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Omezení, která platí během období náhledu

> [!IMPORTANT]
> Pro počáteční fázi programu náhledu pro tuto funkci Microsoft podporuje pouze centra, která mají cloudové jednotky škálování, nikoli centra, která mají hraniční jednotky škálování. Hraniční jednotky škálování jsou instalovány místně a očekává se, že budou k dispozici během nadcházející fáze programu.

Vzhledem k tomu, že jsou cloudové a hraniční jednotky škálování funkcí náhledu, služby, které s nimi souvisí, jsou aktuálně dostupné v omezených zemích a regionech. Povolením cloudových a hraničních jednotek škálování potvrzujete, že chápete, že některá data související s konfigurací a zpracováním cloudových a hraničních jednotek škálování mohou být uložena v datovém centru umístěném v USA. Povolením cloudových a hraničních jednotek škálování také souhlasíte s [podmínkami pro Cloud a Edge Preview pro Finance and Operations](https://Aka.ms/SCMCnETerms). Chcete-li se dozvědět více o cloudových a hraničních jednotkách škálování, projděte si [dokumentaci](https://aka.ms/scmcne).

Vaše soukromí je pro Microsoft důležité. Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů](https://aka.ms/privacy).

> [!IMPORTANT]
> Některé obchodní funkce nejsou ve verzi public preview plně podporovány, když se na jednotkách škálování používá pracovní zatížení. Další informace o nastavení funkčních pracovních zatížení získáte dále v tomto tématu.

## <a name="scale-units-and-dedicated-workloads"></a>Škálování jednotek a vyhrazená pracovní zatížení

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 s jednotkami škálování":::

Jednotky škálování rozšiřují vaše centrální prostředí centra Supply Chain Management přidáním vyhrazené kapacity zpracování. Jednotky škálování mohou běžet v cloudu. Alternativně mohou běžet hraničně ve vašem místním zařízení. Jednotky škálování lze dočasně odpojit od prostředí centra. Když jsou jednotky škálování připojené, obdrží všechny informace, které jsou vyžadovány ke spuštění vyhrazeného zpracování pro přiřazené úlohy.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Možnosti jednotky škálování ve verzi public preview":::

Ve verzi public preview můžete nakonfigurovat prostředí rozbočovače s vybranými úlohami na cloudové jednotce škálování pomocí portálu správce jednotky škálování. Náhled účastníků, kteří mají přístup k místním prostředím Local Business Data (LBD), může také nakonfigurovat prostředí LBD jako hraniční jednotku škálování.

Úloha je definovaná sada obchodních funkcí, kterou lze vyřadit a delegovat na jednotce škálování. V současné době jsou v náhledu k dispozici dva typy úloh:

- Provádění výroby
- Řízení skladu

Každé jednotce škálování můžete přiřadit jeden z každého typu úlohy. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Funkce vyhrazeného pracovního vytížení v jednotce škálování

Při provádění výroby poskytují cloudové a okrajové jednotky škálování následující funkce, i když hraniční jednotky nejsou připojeny ke cloudu:

- Obsluha strojů a vedoucí výroby mají přístup k operačnímu výrobnímu plánu.
- Operátoři strojů mohou udržovat aktuální plán spuštěním samostatných a procesních výrobních úloh.
- Vedoucí dílny může upravit operační plán.
- Pracovníci mají přístup k času a docházce pro označení příchodu a odchodu v hraničním pásmu, aby zajistili správný výpočet platu pracovníka.

Další informace viz [podrobnosti o úloze výrobní jednotky škálování](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Možnosti úlohy vyhrazené správy skladu v jednotce škálování

V případě řízení skladu poskytují cloudové a hraniční jednotky škálování následující funkce, i když hraniční jednotky nejsou připojeny ke cloudu:

- Zpracování vybraných vlnových metod pro prodejní objednávky a doplnění poptávky.
- Pracovníci skladu mohou pomocí mobilní aplikace Řízení skladu spouštět práci ve skladu a poptávku doplnění.
- Pracovníci skladu se mohou dotazovat na vlastní sklad pomocí mobilní aplikace Řízení skladu.
- Pracovníci skladu mohou vytvářet a spouštět pohyby ve skladu pomocí mobilní aplikace Řízení skladu.
- Pracovníci skladu mohou registrovat nákupní objednávky a provádět vyskladnění pomocí mobilní aplikace Řízení skladu.

Další informace viz [podrobnosti o úloze skladové jednotky škálování](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Integrované jednotky škálování pro vaše prostředí Supply Chain Management

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Nasazení náhledu pro cloudové a hraniční jednotky škálování

Následující obrázek ukazuje tok registrace a zřizování pro public preview pro cloudové jednotky škálování.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Náhled kroků registrace":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>Výběr klienta projektu LCS a proces podrobného náhledu

V public preview [Portál správce jednotky škálování](https://aka.ms/SCMSUM) zobrazuje seznam klientů, kterých je váš účet součástí a toho, kde jste vlastníkem nebo správcem prostředí pro projekt LCS.

Pokud klient, kterého hledáte, není v tomto seznamu, přejděte na [LCS](https://lcs.dynamics.com/v2) a ujistěte se, že jste buď správcem prostředí, nebo vlastníkem projektu LCS pro daného klienta. Všimněte si, že pouze účty Azure Active Directory (Azure AD) od vybraného klienta mají oprávnění k dokončení registrace.

> [!NOTE]
> Poté, co použijete změny v LCS, může trvat až 30 minut, než se změny v seznamu klientů projeví.

U každého klienta se v seznamu zobrazuje stav registrace.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Možnost registrace klienta":::

Výběrem odkazu **Kliknutím sem se zaregistrujete** se zaregistrujte v klientovi LCS, abyste se mohli účastnit náhledu. Musíte přijmout podmínky. Musíte také zadat obchodní e-mailovou adresu, na kterou může společnost Microsoft odesílat komunikaci související s procesem registrace náhledu.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Předložení registrace klienta":::

Microsoft zkontroluje váš požadavek a bude vás informovat o dalších krocích zasláním e-mailu na adresu, kterou jste uvedli v registračním formuláři.

Poté, co vám bude udělen přístup k programu náhledu, obdržíte dva promo kódy pro váš projekt LCS. Tyto promo kódy nyní můžete použít k nasazení dvou prostředí v LCS. Prostředí musí používat verzi PEAP 10.0.15 nebo novější. Po dokončení použití propagačních kódů informujte společnost Microsoft (podle pokynů), abychom mohli dokončit povolení prostředí pro funkce náhledu. Po dokončení tohoto kroku konfigurace vás společnost Microsoft upozorní.

Nyní můžete začít konfigurovat jednotky škálování a pracovní vytížení v prostředí náhledu.

> [!IMPORTANT]
> Když konfigurujete cloudové jednotky škálování, můžete [provést všechny požadované kroky na portálu správce jednotky škálování](#scale-unit-manager-portal).
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Správa cloudových jednotek škálování a úkolů pomocí portálu správce jednotky škálování

Přejděte na [portál správce jednotky škálování](https://aka.ms/SCMSUM) a přihlaste se pomocí účtu klienta. Na stránce **Konfigurovat jednotky škálování** můžete přidat prostředí centra, pokud ještě není uvedeno. Poté můžete vybrat centrum, které chcete konfigurovat pomocí jednotek škálování a úloh.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Zkušenosti se správou jednotky škálování a úlohy":::

Chcete-li přidat jednu nebo více jednotek škálování, které jsou k dispozici ve vaší topologii, vyberte **Přidat jednotky škálování**. V náhledu byste měli vidět cloudovou jednotku škálování, kterou jste nasadili z jednoho z promo kódů, které jste obdrželi v rámci programu náhledu.

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Na kartě **Definované úlohy** pomocí tlačítka **Vytvořit úlohu** přidejte správu skladu nebo úlohu provedení výroby do některé z jednotek škálování. U každé úlohy musíte určit kontext procesů, které bude úloha vlastnit. Pro úlohy správy skladu je kontextem konkrétní sklad na konkrétním místě a právnické osobě. Pro výrobní pracovní úlohy je kontext konkrétní místo v právnické osobě.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Vytvoření úlohy":::

> [!IMPORTANT]
> Portál správce jednotky škálování v náhledu vám nedovolí odebrat úlohy z jednotek škálování nebo zrušit přiřazení jednotky škálování z centra po provedení přiřazení. Pokud musíte úkol odebrat, požádejte o správu programu náhledu svou kontaktní osobu.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]