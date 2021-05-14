---
title: Přehled správy obchodních dokumentů
description: Toto téma obsahuje informace o použití funkce správy obchodních dokumentů v rámci architektury elektronického výkaznictví.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c691e89a932e683c916eca72f726d9b4fab93181
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944382"
---
# <a name="business-document-management-overview"></a>Přehled správy obchodních dokumentů

[!include [banner](../includes/banner.md)]

Podnikový uživatelé používají [architekturu elektronického výkaznictví](general-electronic-reporting.md) ke konfiguraci formátů pro odchozí dokumenty v souladu s právními požadavky různých zemí a oblastí. Uživatelé mohou rovněž definovat tok dat, který určuje, která data aplikace budou umístěna do generovaných dokumentů. Architektura elektronického výkaznictví generuje odchozí dokumenty ve formátech Microsoft Office (sešity aplikace Excel nebo dokumenty aplikace Word) pomocí předdefinovaných šablon. Šablony jsou naplněny požadovanými daty v souladu s konfigurovaným tokem dat, když jsou vygenerovány požadované dokumenty. Každý konfigurovaný formát lze publikovat jako součást řešení elektronického vykazování pro generování určitých odchozích dokumentů. To je představováno konfigurací formátu elektronického vykazování, která může obsahovat šablony, které lze použít k vygenerování různých odchozích dokumentů. Podnikoví uživatelé mohou pomocí této architektury spravovat požadované obchodní dokumenty.

**Správa obchodních dokumentů** je vytvořena na vrcholu systému architektury elektronického výkaznictví a umožňuje podnikovým uživatelům upravovat šablony obchodních dokumentů pomocí služby Microsoft 365 nebo příslušné desktopové aplikace Microsoft Office. Úpravy dokumentů mohou zahrnovat změny návrhů obchodních dokumentů a přidávání zástupných symbolů pro další data bez změn zdrojových kódů a nových nasazení. K aktualizaci šablon obchodních dokumentů nejsou vyžadovány žádné znalosti architektury elektronického vykazování.

> [!NOTE]
> Berte na vědomí, že správa obchodních dokumentů umožňuje měnit šablony, které se používají k vytváření obchodních dokumentů, jako jsou objednávky, faktury atd. Zatímco byla šablona upravena a byla publikována její nová verze, tato verze se použije k vygenerování požadovaných obchodních dokumentů. Správu obchodních dokumentů nelze použít k úpravě již generovaných obchodních dokumentů.

## <a name="supported-deployments"></a>Podporovaná nasazení

V současné době je funkce správy obchodních dokumentů implementována pouze pro nasazení v cloudu. Pokud je tato funkce důležitá pro vaše místní nasazení, dejte nám vědět na webu [Nápady](https://experience.dynamics.com/ideas/), kde můžete poskytovat zpětnou vazbu.

## <a name="supported-microsoft-office-applications"></a>Podporované aplikace Microsoft Office

Chcete-li použít správu obchodních dokumentů pro úpravy šablon ve formátech Excel nebo Word pomocí desktopových aplikací Microsoft Office, je nutné mít nainstalováno Microsoft Office 2010 nebo novější verzi. Je to podporováno v cloudových a místních nasazeních.

Chcete-li použít správu obchodních dokumentů pro úpravy šablon ve formátech Excel nebo Word pomocí aplikací Microsoft 365, je nutné mít nainstalován Microsoft 365 Office pro webové předplatné. To je podporováno v cloudovém nasazení.

## <a name="business-document-availability"></a>Dostupnost obchodních dokumentů

Úplný seznam všech sestav plánovaných pro vydání v říjnu 2019 najdete v části [Konfigurovatelné vykazování obchodních dokumentů v aplikacích Word a Excel](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

Úplný seznam všech sestav plánovaných pro vydání v říjnu 2020 najdete v části [Konfigurovatelné vykazování obchodních dokumentů - šablony Word](/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Další sestavy budou k dispozici v budoucích verzích. Zvláštní oznámení o dalších sestavách budou odeslána samostatně. Informace o tom, jak zkontrolovat seznam aktuálně dostupných sestav, najdete v části [Seznam konfigurací ER, které byly vydány v aplikaci Finance na podporu konfigurovatelných obchodních dokumentů](#list-of-configurations-cbd) níže.

Chcete-li získat další informace o této funkci, vyplňte příklad tomto tématu.

## <a name="configure-er-parameters"></a>Konfigurace parametrů ER

Vzhledem k tomu, že správa obchodních dokumentů je na vrcholu architektury elektronického výkaznictví, je nutné parametry elektronického výkaznictví nakonfigurovat tak, aby začaly spolupracovat se správou obchodních dokumentů. Nejprve je třeba nastavit parametry elektronického výkaznictví, jak je popsáno v tématu [Konfigurace architektury elektronického výkaznictví (ER)](electronic-reporting-er-configure-parameters.md). Je také nutné přidat nového poskytovatele konfigurace, jak je popsáno v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Pracovní prostor elektronického výkaznictví](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Import řešení elektronického výkaznictví

V příkladu tohoto postupu jsou použity ukázkové konfigurace ER. Do aktuální instance aplikace Dynamics 365 Finance je nutné importovat konfigurace ER obsahující šablony obchodních dokumentů, které lze upravit pomocí správy obchodních dokumentů. Chcete-li provést tento postup, stáhněte a uložte následující soubory.

**Ukázka fakturačního řešení elektronického výkaznictví pro zákazníky**

| Soubor                                      | Obsah |
|-------------------------------------------|---------|
| Customer invoicing model.version.2.xml    | [Konfigurace datového modelu elektronického výkaznictví](https://download.microsoft.com/download/b/f/a/bfa5cb52-e6e2-42bc-a4c0-77014a4c54e6/Customerinvoicingmodel.version.2.xml) |
| Customer FTI report (GER).version.2.3.xml | [Konfigurace formátu elektronického výkaznictví volné faktury](https://download.microsoft.com/download/3/c/2/3c2e58f2-6e56-43d9-85ea-4c97252a108d/CustomerFTIreportGER.version.2.3.xml) |

**Ukázka řešení platebních šeků elektronického výkaznictví**

| Soubor                                     | Obsah |
|------------------------------------------|---------|
| Model for cheques.version.10.xml         | [Konfigurace datového modelu elektronického výkaznictví](https://download.microsoft.com/download/3/7/6/376cb0f6-181a-4895-a432-390ffca64162/Modelforcheques.version.10.xml) |
| Cheques printing format.version.10.9.xml | [Konfigurace formátu elektronického výkaznictví platebního šeku](https://download.microsoft.com/download/6/d/6/6d61bfff-3d89-4377-9e34-2e3ee6d6df91/Chequesprintingformat.version.10.9.xml) |

**Ukázka řešení zahraničního obchodu elektronického výkaznictví**

| Soubor                             | Obsah |
|----------------------------------|---------|
| Intrastat model.version.1.xml    | [Konfigurace datového modelu elektronického výkaznictví](https://download.microsoft.com/download/2/0/0/200d6ed1-eff8-48ec-ab75-175a4acf9714/Intrastatmodel.version.1.xml) |
| Intrastat report.version.1.9.xml | [Konfigurace formátu elektronického výkaznictví sestavy řízení systému Intrastat](https://download.microsoft.com/download/7/a/2/7a2a27c3-a8a5-42a1-9d04-f0a8e1ec1707/Intrastatreport.version.1.9.xml) |

K importu každého souboru použijte následující postup. Před importem odpovídající *konfigurace* elektronického výkaznictví importujte pro jednotlivá řešení elektronického výkaznictví konfiguraci *datového modelu* elektronického výkaznictví v tabulkách výše.

1. Otevřete stránku **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. V horní části stránky vyberte možnost **Směna**.
3. Vyberte **Načíst ze souboru XML**.
4. Výběrem možnosti **Procházet** načtete požadovaný soubor XML.
5. Kliknutím na tlačítko **OK** potvrďte import konfigurace.

![Import konfigurace stránky potvrzující konfigurace ER](./media/BDM-Overview-ERSolutions.png)

Případně můžete importovat oficiálně publikovaná konfigurace formátu ER ze služby Microsoft Dynamics Lifecycle Service (LCS). Chcete-li například dokončit tento postup, můžete importovat nejnovější verzi konfigurace formátu ER **Volná textová faktura (Excel)**. Odpovídající datové modely ER a konfigurace mapování modelu ER budou importovány automaticky.

![Stránka obsahu Knihovna sdílených datových zdrojů LCS](./media/BDM-Overview-SharedAssetLibrary.png)

Další informace o importu konfigurací elektronického výkaznictví naleznete v tématu [Správa životního cyklu konfigurace elektronického výkaznictví](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Povolení správy obchodních dokumentů

Chcete-li zahájit správu obchodních dokumentů, musíte otevřít pracovní prostor **Správa funkcí** a povolit funkci **Správa obchodních dokumentů**.

Chcete-li povolit funkci správy obchodních dokumentů pro všechny právnické osoby, použijte následující postup.

1. Otevřete pracovní prostor **Správa funkcí**.
2. Na kartě **Nová** v seznamu funkci **Správa obchodních dokumentů**.
3. Výběrem možnosti **Povolit nyní** zapněte vybranou funkci.
4. K nové funkci budete mít přístup po aktualizaci stránky.

> [!NOTE]
> Další informace o použití nového uživatelského rozhraní dokumentu v modulu Správa obchodních dokumentů naleznete v tématu [Nové uživatelské rozhraní dokumentů v modulu Správa obchodních dokumentů](er-business-document-management-new-template-ui.md).

![Pracovní prostor Správa funkcí](./media/BDM-Overview-FMEnabling.png)

Další informace o aktivaci nových funkcí naleznete v tématu [Přehled správy funkcí](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Konfigurace parametrů

Chcete-li nastavit základní parametry pro správu obchodních dokumentů, použijte informace v následujících sekcích.

### <a name="prerequisites-for-parameter-setup"></a>Předpoklady pro nastavení parametrů

Před nastavením správy obchodních dokumentů je nutné nastavit v architektuře správy dokumentů požadovaný typ dokumentu. Tento typ dokumentu se používá k určení dočasného úložiště dokumentů ve formátech Office (Excel a Word), které se používají jako šablony pro sestavy elektronického výkaznictví. Dočasné šablony úložiště lze upravit pomocí desktopových aplikací Office.

Pro tento typ dokumentu je nutné vybrat následující hodnoty atributů.

| Název atributu | Hodnota atributu |
|----------------|-----------------|
| Třída          | Připojit soubor     |
| Seskupit          | Soubor            |
| Umístění       | SharePoint      |

Informace o nastavení požadovaných parametrů správy dokumentů a typů dokumentů naleznete v tématu [Konfigurace správy dokumentů](../../fin-ops/organization-administration/configure-document-management.md).

![Nastavení typu dokumentu pro správu dokumentů](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Nastavení parametrů

Na stránce **parametry obchodního dokumentu** lze nastavit základní parametry správy obchodních dokumentů. Na stránku mohou přistupovat jen někteří uživatelé. Mezi ně patří:

- Uživatelé s rolí **Správce systému**.
- Uživatelé s libovolnou rolí s oprávněním **Údržba parametrů správy obchodních dokumentů** (název AOT **ERBDMaintainParameters**).

Pomocí následujícího postupu nastavíte základní parametry pro všechny právnické osoby.

1. Přihlaste se jako uživatel s přístupem na stránku **Parametry obchodního dokumentu**.
2. Přejděte do části **Správa organizace** \> **Elektronické vykazování** \> **Správu obchodních dokumentů** \> **Parametry obchodního dokumentu**.
3. Na stránce **Parametry obchodního dokumentu** na kartě **Přílohy** v poli **Typ dokumentu SharePoint** definujte typ dokumentu, který se má použít k dočasnému uložení šablon ve formátech Office v době, kdy jsou upravovat pomocí desktopových aplikací Office. 

> [!NOTE]
> Pro tento parametr jsou k dispozici pouze typy dokumentů, které jsou konfigurovány s použitím umístění SharePoint.

![Nastavení parametrů správy obchodních dokumentů](./media/BDM-Overview-BDMSetting.png)

Vybraný typ dokumentu je specifický pro společnost a bude použit, pokud uživatel pracuje se správou obchodních dokumentů ve společnosti, pro kterou je nastaven vybraný typ dokumentu. Pokud uživatel pracuje se správou obchodních dokumentů v jiné společnosti, bude použit stejný vybraný typ dokumentu, pokud nebyl pro tuto společnost konfigurován jiný. Pokud byl typ dokumentu konfigurován, bude použit namísto typu vybraného v poli **Typ dokumentu SharePoint**.

> [!NOTE]
> Parametr **Typ dokumentu SharePoint** definuje složku SharePoint jako dočasné úložiště pro šablony, které lze upravovat pomocí aplikací Microsoft Excel nebo Word. Tento parametr je nutné nastavit, pokud chcete používat tyto desktopové aplikace Office pro úpravy šablon. Další informace naleznete v tématu [Úprava šablony v desktopové aplikaci Office](#EditInOfficeDesktopApp). Chcete-li upravit šablonu pouze pomocí funkce v aplikaci Microsoft 365, můžete tento parametr ponechat prázdný. Další informace naleznete v tématu [Úprava šablony v Microsoft 365](#EditInOffice365).

## <a name="configure-access-permissions"></a>Konfigurace přístupových oprávnění

Ve výchozím nastavení, pokud není povolen přístup k oprávněním pro správu obchodních dokumentů, uvidí každý uživatel s přístupem k pracovnímu prostoru správy obchodních dokumentů všechny šablony řešení elektronického výkaznictví, které jsou k dispozici. Pracovní prostor správy obchodních dokumentů zobrazí pouze ty šablony, které se nacházejí v konfiguracích formátu elektronického výkaznictví a jsou označeny značkou **Typ obchodního dokumentu**.

![Stránka konfigurace ER se značkou typu obchodního dokumentu](./media/BDM-Overview-ERFormatTags.png)

Seznam šablon, které jsou k dispozici v pracovním prostoru správy obchodních dokumentů, může být omezen konfigurací přístupových oprávnění. To může být důležité v případě, že se k vytváření obchodních dokumentů pro různé obchodní domény (funkční oblasti) používají různé šablony a určitým uživatelům chcete umožnit přístup k různým šablonám pro úpravy v pracovním prostoru správy obchodních dokumentů.

Přístupová oprávnění ke správě obchodních dokumentů lze nastavit v **konfigurátoru přístupových oprávnění**. Na stránku mohou přistupovat jen následující uživatelé:

- Uživatelé s rolí **Správce systému**.
- Uživatelé s jakoukoli jinou rolí s oprávněním **Konfigurace oprávnění pro přístup k úpravám šablon obchodních dokumentů** (název AOT **ERBDTemplatesSecurity**).

Chcete-li povolit nastavit přístupová oprávnění ke správě obchodních dokumentů pro všechny právnické osoby, použijte následující postup.

1. Přihlaste se jako uživatel s přístupem na stránku **Konfigurátor přístupových oprávnění**.
2. Přejděte do části **Správa organizace** \> **Elektronické vykazování** \> **Správu obchodních dokumentů** \> **Správa přístupových oprávnění**.

    Věnujte pozornost oznámením, která vás informují, že použití přístupových oprávnění pro správu obchodních dokumentů není aktuálně povoleno.

    ![Stránka konfigurátoru přístupových oprávnění ke správě obchodních dokumentů](./media/BDM-Overview-TemplatesAccess1.png)

    Při tomto nastavení může každý uživatel s libovolnou rolí zabezpečení s oprávněním pro **správu šablon obchodních dokumentů** (název AOT **ERBDManageTemplates**) otevřít pracovní prostor správy obchodních dokumentů a upravit libovolnou šablonu, která je k dispozici.

    Následující obrázek zobrazuje informace, které jsou k dispozici v pracovním prostoru Správa obchodních dokumentů pro uživatele s rolí **Úředník pohledávek**. S aktuálním nastavením přístupových oprávnění může uživatel upravovat šablony obchodních dokumentů z různých funkčních oblastí, včetně fakturace, regulačního vykazování a plateb.

    ![Stránka pracovního prostoru správy obchodních dokumentů pro úředníka pohledávek](./media/BDM-Overview-TemplatesForAlice1.png)

3. Na stránce **Konfigurátor přístupových oprávnění** vyberte možnost **Nastavení oprávnění přístupu**.
4. V dialogovém okně **Nastavení přístupových oprávnění pro úpravy šablon** povolte možnost **Použít konfigurovaná přístupová oprávnění**.
5. Klepnutím na tlačítko **OK** potvrďte, že byla povolena oprávnění přístupu ke správě obchodních dokumentů.

    ![Stránka potvrzení přístupových oprávnění ke správě obchodních dokumentů](./media/BDM-Overview-TemplatesAccess2.png)

6. Chcete-li zadat novou obchodní roli, pro kterou mají být konfigurována oprávnění pro přístup k šablonám správy obchodních dokumentů, vyberte možnost **Přidat**.
7. V dialogovém okně **Role zabezpečení** vyberte roli **Úředník pohledávek** a poté klepnutím na tlačítko **OK** potvrďte výběr role.
8. Na kartě **Přístupová oprávnění dle značek konfigurací** vyberte možnost **Nové**.
9. V poli **Typ značky** vyberte možnost **Funkční oblast** a v poli **ID** vyberte možnost **Fakturace**.
10. Chcete-li uložit konfigurovaná přístupová oprávnění pro vybranou roli, vyberte možnost **Uložit**.

    Aktuální nastavení znamená, že pro každého uživatele, který má roli **Úředník pohledávek** a funkční oprávnění **Správa šablon obchodních dokumentů** (název AOT **ERBDManageTemplates**), šablony konfigurací elektronického výkaznictví, které mají hodnotu **Fakturace** pro značku **Funkční oblast**, budou k dispozici pro úpravy v pracovním prostoru Správa obchodních dokumentů.

11. Přepněte podokno **Související informace** z pravé strany aktuální stránky. V podokně **Související informace** je zobrazen způsob použití konfigurovaných přístupových oprávnění včetně informací o tom, jaké konfigurační šablony elektronického výkaznictví budou k dispozici pro uživatele s rolí **Úředník pohledávek**.

    ![Podokno souvisejících informací na stránce Konfigurátor přístupových oprávnění](./media/BDM-Overview-TemplatesAccess3.png)

12. Na kartě **Přístupová oprávnění dle konfigurací** vyberte možnost **Přidat**.
13. V dialogovém **Výběr konfigurace** označte konfiguraci formátu elektronického výkaznictví jako **Sestavu Intrastat**.
14. Kliknutím na tlačítko **OK** potvrďte zadání vybraných konfigurací a výběrem možnosti **Uložit** uložte konfigurovaná přístupová oprávnění pro vybranou roli.

Aktuální nastavení znamená, že pro každého uživatele, který má roli **Úředník pohledávek** a funkční oprávnění **Správa šablon obchodních dokumentů** (název AOT **ERBDManageTemplates**), následující šablony budou k dispozici pro úpravy v pracovním prostoru Správa obchodních dokumentů:

- Šablony, které mají hodnotu **Fakturace** pro značku **Funkční oblast**.
- Šablony z konfigurací formátu elektronického výkaznictví, které jsou uvedeny na kartě **Přístupová oprávnění dle konfigurací** (šablony z konfigurace formátu **Sestava Intrastat** domény **Statutární vykazování** v tomto příkladu).

![Pevné záložky přístupových oprávnění na stránce Konfigurátor přístupových oprávnění.](./media/BDM-Overview-TemplatesAccess4.png)

Následující obrázek zobrazuje, co pracovní prostor Správa obchodních dokumentů umožňuje uživateli s rolí **Úředník pohledávek**. S aktuálním nastavením přístupového oprávnění ke správě obchodních dokumentů může uživatel upravovat šablony obchodních dokumentů z domény **Fakturace** a z konfigurace formátu elektronického výkaznictví **Sestava Intrastat**. Šablony z domény **Platby** nejsou přístupné pro roli **Úředník pohledávek**.

![Stránka pracovního prostoru Úprava šablon obchodních dokumentů ve správě obchodních dokumentů](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> Pravidla **Přístupová oprávnění dle konfigurací** jsou uložena za pomoci jedinečného ID konfigurace formátu elektronického výkaznictví. To znamená, že tato pravidla nebudou odstraněna, pokud konfigurace elektronického výkaznictví, která na ně odkazuje, bude odstraněna. Při importu odstraněných konfigurací zpět do této instance budou tato pravidla na ně odkazovat znovu. Po opětovném importu odstraněných konfigurací není nutné pravidla nastavovat znovu.

## <a name="use-business-document-management-to-edit-templates"></a>Použití správy obchodních dokumentů k úpravě šablon

Podnikoví uživatelé mají přístup k šablonám obchodních dokumentů pro úpravy v pracovním prostoru správy obchodních dokumentů. K pracovnímu prostoru správy obchodních dokumentů mohou přistupovat pouze následující uživatelé:

- Uživatelé s rolí **Správce systému**.
- Uživatelé s libovolnou rolí s oprávněním **Správa šablon obchodních dokumentů** (název AOT **ERBDManageTemplates**).

Následující postup slouží k šablon volných faktur v pracovním prostoru správy obchodních dokumentů. Před provedením tohoto postupu je nutné provést všechny předchozí postupy uvedené v tomto tématu.

1. Přihlaste se jako uživatel s přístupem do pracovního prostoru Řízení obchodního dokumentu.
2. Otevřete pracovní prostor správy obchodních dokumentů.

Pokud je funkce **Prostředí UI podobné systému Office pro správu obchodního dokumentu** vypnuta v pracovním prostoru **Správa funkcí**, hlavní mřížka v pracovním prostoru **Správa obchodních dokumentů** zobrazuje následující šablony:

- Šablony, které vlastní váš poskytovatel konfigurace aplikace ER (tj. poskytovatel, který je aktuálně označen jako aktivní v pracovním prostoru **Elektronického vykazování**). Po vybrání jedné z těchto šablon můžete vybrat možnost **Upravit šablonu** a začít ji upravovat.
- Šablony vlastněné ostatními poskytovateli konfugurace ER. Po vybrání jedné z těchto šablon můžete vybrat **Nový dokument**, abyste vytvořili jeho kopii, která je vlastněna vaším poskytovatelem konfigurace ER, a poté můžete začít upravovat jeho kopii.

![Stránka Seznam šablon v pracovním prostoru Správa obchodních dokumentů](./media/BDM-Overview-EditingTemplate1.png)

Na kartě **Šablony** se zobrazí obsah vybrané šablony. Vyberte kartu **Podrobnosti**, na které si můžete prohlédnout podrobnosti o vybrané šabloně a podrobnosti o konfiguraci formátu elektronického výkaznictví, kde je tato šablona umístěna. Všimněte si, že všechny šablony mají stav **Publikováno** a neobsahují údaje ve sloupci **Revize**. To znamená, že tyto šablony aktuálně nejsou upravovány.

Pokud je funkce **Prostředí UI podobné systému Office pro správu obchodního dokumentu** zapnuta v pracovním prostoru **Správa funkcí**, hlavní mřížka v pracovním prostoru **Správa obchodních dokumentů** zobrazuje šablony, které jsou vlastněny vaším poskytovatelem konfigurace ER (tj. poskytovatelem, který je aktuálně označen jako aktivní v pracovním prostoru **Elektronického vykazování**). Po vybrání jedné z těchto šablon můžete vybrat možnost **Upravit šablonu** a začít ji upravovat.

Chcete-li pracovat se šablonami, které jsou vlastněny jinými zprostředkovateli konfigurace ER, vyberte možnost **Nový dokument** a vytvořte kopii šablony, která je vlastněna vaším poskytovatelem ER. Poté můžete začít upravovat kopii. Další informace naleznete v tématu [Nové uživatelské rozhraní dokumentu v modulu Správa obchodních dokumentů](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Zahájení úprav šablon vlastněných vaším poskytovatelem konfigurace

1. V pracovním prostoru Správa obchodních dokumentů vyberte v seznamu šablonu **Formát tisku šeků**.
2. Zvolte kartu **Podrobnosti**.

![Stránka pracovního prostoru správy obchodních dokumentů, karta Podrobnosti](./media/BDM-Overview-EditingTemplate2.png)

Pro vybranou šablonu je k dispozici možnost **Upravit šablonu**. Tato možnost je vždy k dispozici pro šablonu v konfiguraci formátu elektronického výkaznictví, která je vlastněna aktivním poskytovatelem konfigurace elektronického výkaznictví (v tomto případě **Litware, Inc.**). Je -li vybrána možnost **Upravit šablonu**, budete moci upravit existující šablonu z verze konceptu základní konfigurace formátu elektronického výkaznictví.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Zahájení úprav šablon vlastněných ostatními poskytovateli

1. V pracovním prostoru správy obchodních dokumentů vyberte dokument, který chcete použít jako šablonu.

    ![Stránka Vybrat dokument v pracovním prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingTemplate3.png)

2. Vyberte **Nový dokument** a v poli **Název** změňte v případě potřeby název upravitelné šablony. Text se použije k pojmenování konfigurace formátu elektronického výkaznictví, která je automaticky vytvořena. Všimněte si, že verze konceptu této konfigurace **(Kopie sestavy FTI odběratele (GER)kopie**), která bude obsahovat upravenou šablonu, bude automaticky označena pro spuštění tohoto formátu elektronického výkaznictví pro aktuálního uživatele. Zároveň bude původní neupravená šablona ze základní konfigurace formátu elektronického výkaznictví použita ke spuštění tohoto formátu elektronického výkaznictví pro libovolného jiného uživatele.
3. V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.
4. V poli **Komentář** změňte komentář pro automaticky vytvořenou revizi upravitelné šablony.
5. Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.

![Potvrzení začátku procesu úprav a k vytvoření nové šablony](./media/BDM-Overview-EditingTemplate4.png)

Pokud neexistuje žádný poskytovatel, bude nabídnuto vytvoření. Pokud neexistuje žádný aktivní poskytovatel, bude nabídnuta možnost jeho aktivace.

Chcete-li vytvořit poskytovatele, změňte název poskytovatele v poli **Název**, aktualizujte internetovou adresu nového poskytovatele v poli **Internetová adresa** a vyberte **OK** k potvrzení.

   ![Vytvoření nového poskytovatele v BDM](./media/bdm_create_provider.png)

Chcete-li aktivovat stávajícího poskytovatele, vyberte jeho jméno v poli **Poskytovatel konfigurace** a vyberte **OK** k nastavení poskytovatele jako aktivního.

   ![Aktivace poskytovatele v BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> Každá šablona BDM bude odkazovat na zprostředkovatele jako na autora konfigurace. Proto je pro šablonu vyžadován aktivní poskytovatel.


Možnost **Nový dokument** je vždy k dispozici pro šablonu v konfiguraci formátu elektronického výkaznictví poskytovanou aktuálním a jiným poskytovatelem (v tomto případě Microsoft), který nemá žádnou revizi. Upravená šablona bude poté uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.



### <a name="start-editing-a-template"></a>Zahájení úpravy šablony

1. Z vybrané šablony vyberte možnost **Upravit dokument**.
2. V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.
3. V poli **Komentář** změňte poznámku pro automaticky vytvořenou revizi upravitelné šablony.

    ![Stránka Úprava šablony v pracovním prostoru Správa obchodních dokumentů](./media/BDM-Overview-EditingTemplate5.png)

4. Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.

Otevře se stránka **Editor šablony BDM**. Vybraná šablona bude k dispozici pro online úpravy pomocí Microsoft 365.

![Stránka editoru šablon pro správu obchodních dokumentů](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Úprava šablony pomocí Microsoft 365

Šablonu můžete upravit pomocí aplikace Microsoft 365. Například v řešení Office Online změníte písmo výzev polí v záhlaví šablony z **Obyčejné** na **Tučné**. Tyto změny se automaticky uloží v upravitelné šabloně, která se nachází v úložišti primární šablony (standardně úložiště objektu blob služby Azure). To je konfigurováno pro rámec elektronického výkaznictví.

![Změna písma na tučné v záhlaví šablony na stránce editoru šablon správy obchodních dokumentů](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Úprava šablony v desktopové aplikaci Office

> [!NOTE]
> Tato funkce je k dispozici pouze tehdy, když je parametr **Typ dokumentu SharePoint** správně nakonfigurován. Další informace naleznete v tématu [Konfigurace parametrů](#SetupBdmParameters).

1. Chcete- li upravit šablonu pomocí funkce desktopové aplikace Office (v tomto příkladu aplikace Excel), vyberte možnost **Otevřít v desktopové aplikaci**. Upravitelná šablona je zkopírována z trvalého úložiště do dočasného úložiště konfigurovaného v parametrech správy obchodních dokumentů jako složka SharePoint.
2. Potvrďte, že chcete otevřít šablonu z dočasného úložiště souborů v desktopové aplikaci Office Excel.

    ![Šablona otevřená v desktopové aplikaci Excel](./media/BDM-Overview-EditingLayout3.png)

3. Upravte šablonu. Například změňte barvu písma výzev polí v záhlaví šablony z **Černá** na **Modrá**.

    ![Úprava barvy písma v záhlaví šablony pomocí desktopové aplikace Excel](./media/BDM-Overview-EditingLayout4.png)

4. Volbou **Uložit** v desktopové aplikaci Excel uložte změny šablony do dočasného úložiště.

    ![Uložení změn na stránce editoru šablon pro správu obchodních dokumentů pomocí desktopové aplikace Excel](./media/BDM-Overview-EditingLayout5.png)

5. Zavřete desktopovou aplikaci Excel.
6. Výběrem možnosti **Synchronizovat uloženou kopii** synchronizujte dočasné úložiště šablon s trvalým úložištěm šablon.

> [!NOTE]
> Kopie upravitelné šablony v dočasném úložišti souborů je uchována pouze po aktuální relaci úpravy šablony. Po dokončení této relace zavřením stránky **Editor šablon BDM** bude tato kopie odstraněna. Pokud jste upravili šablonu v dočasném úložišti souborů a nevybrali možnost **Synchronizovat uloženou kopii**, při pokusu o zavření stránky **Editor šablon BDM** se zobrazí zpráva s dotazem, zda chcete zavedené změny uložit. Chcete-li uložit změny šablony do trvalého umístění souboru, vyberte možnost **Ano**.

### <a name="validate-a-template"></a>Ověření šablony

1. Na stránce **Editor šablon BDM** vyberte možnost **Zkontrolovat problémy** pro ověření upravené šablony s použitím základní konfigurace formátu elektronického výkaznictví. Chcete-li šablonu zarovnat se strukturou formátu ze základní konfigurace formátu elektronického výkaznictví, postupujte podle doporučení (pokud existují).
2. Chcete-li zobrazit aktuální strukturu formátu ze základní konfigurace formátu elektronického výkaznictví, která musí být zarovnána s upravitelnou šablonou, vyberte možnost **Zobrazit formát**. 
3. Chcete-li podokno zavřít, vyberte možnost **Skrýt formát**.

    ![Stránka Editor šablony BDM](./media/BDM-Overview-EditingTemplate6.png)

4. Zavřete stránku **Editor šablony BDM**.

Aktualizovaná šablona je zobrazena na kartě **Šablona** . Všimněte si, že stav upravené šablony je nyní **Koncept** a aktuální revize již není prázdná. To znamená, že proces úpravy této šablony byl zahájen.

![Zobrazení aktualizované šablony na stránce Seznam šablon v pracovním prostoru Správa obchodních dokumentů](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Test upravené šablony 

1. V aplikaci změňte položku na společnost **USMF**.
2. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
3. Vyberte fakturu **FTI-00000002** a poté vyberte možnost **Správatisku**.
4. Chcete-li určit rozsah faktur, které mají být zpracovány, vyberte **Modul – Pohledávky** \> **Dokumenty** \> **Volná faktura** \> **Původní dokument**.
5. V poli **Formát sestavy** vyberte formát elektronického výkaznictví **Kopie sestavy FTI odběratele (GER)** pro zadanou úroveň dokumentu.

    ![Stránka nastavení správy tisku](./media/BDM-Overview-TestRun1.png)

6. Stisknutím klávesy **Escape** zavřete aktuální stránku.
7. Vyberte možnost **Tisk** a poté vyberte možnost **Vybráno**.
8. Stáhněte dokument a otevřete jej pomocí desktopové aplikace Excel.

![Stránka Volné faktury](./media/BDM-Overview-TestRun2.png)

Upravená šablona slouží k vygenerování sestavy volné faktury pro vybranou položku. Chcete-li analyzovat, jak je tato sestava ovlivněna změnami, které jste provedli v šabloně, můžete tuto sestavu spustit v jedné relaci aplikace přímo po změně šablony v jiné relaci aplikace.

### <a name="create-an-alternative-template-revision"></a>Vytvoření alternativní revize šablony

1. Otevřete stránku **Editor šablon BDM** a vyberte šablonu **Kopie šablony FTI odběratele (GER)**.
2. Na kartě **Revize** vyberte možnost **Nová**.
3. V případě potřeby změňte v poli **Název** název druhé revize a založte jej na aktuálně aktivní první revizi.
4. Pokud je třeba, v poli **Komentář** změňte poznámku pro automaticky vytvořenou revizi upravitelné šablony.

    ![Vytvoření revizí šablony na stránce Seznam šablon v pracovním prostoru Správa obchodních dokumentů](./media/BDM-Overview-AddRevision.png)

    Vytvořili jste novou revizi šablony, která byla uložena v trvalém úložišti šablon. Nyní můžete pokračovat v úpravách šablony druhé revize, která je aktuálně vybrána jako aktivní.

5. Vyberte první revizi a poté vyberte **Nastavitjako aktivní**. Chcete-li se kdykoli vrátit k revizi šablony, můžete vybrat jinou revizi jako aktivní.
6. Vyberte druhou revizi a poté vyberte možnost **Odstranit**.
7. Tlačítkem **OK** potvrďte, že si opravdu přejete odstranit vybranou revizi. Veškeré neaktivní revize, které již nejsou potřeba, můžete je odstranit.

### <a name="delete-a-modified-template"></a>Odstranění upravené šablony

1. Na stránce **Editor šablon BDM** vyberte kartu **Šablona**.
2. Zvolte **Odstranit**.
3. Pokud klepnutím na tlačítko **OK** potvrďte odstranění, bude odstraněn formát elektronického výkaznictví **Kopie sestavy FTI odběratele (GER)** s upravenou šablonou. Chcete-li prozkoumat ostatní možnosti, vyberte možnost **Storno**.

### <a name="revoke-changes-of-template"></a>Odvolání změn šablony

Při úpravě šablony z formátu elektronického výkaznictví, který vlastní aktuální aktivní zprostředkovatel, vám bude nabídnuta možnost odvolání změn provedených v šabloně.

![Odmítnutí změn šablony na stránce Seznam šablon v pracovním prostoru Správa obchodních dokumentů](./media/BDM-Overview-RevokeChanges.png)

1. Na stránce **Editor šablon BDM** vyberte kartu **Šablona**.
2. Vyberte možnost **Zpět**.
3. Pokud vyberete možnost **OK** k odvolání změn provedených v šabloně, upravená šablona bude nahrazena původní šablonou a všechny změny budou odebrány. Pokud odvoláte změny šablony, budete moci šablonu odstranit. Chcete-li prozkoumat ostatní možnosti, vyberte možnost **Storno**.

### <a name="publish-a-modified-template"></a>Publikování upravené šablony

1. Na stránce **Editor šablon BDM** na kartě **Šablona** vyberte **Publikovat**.
2. Vyberete-li možnost **OK** pro potvrzení publikování, draft odvozeného formátu elektronického výkaznictví **Kopie sestavy FTI odběratele (GER)**, který obsahuje upravenou šablonu, bude označen jako dokončený. Upravená šablona bude k dispozici pro ostatní uživatele. Dokončené verze tohoto formátu elektronického výkaznictví zachovají pouze poslední aktivní revizi vaší šablony. Ostatní revize budou odstraněny. Chcete-li prozkoumat ostatní možnosti, vyberte možnost **Storno**.

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Vybral jsem možnost Upravit dokument, ale namísto přechodu na stránku Editor šablon BDM v aplikaci Finance jsem byl přesměrován na webovou stránku Microsoft 365.

Jedná se o známý problém s přesměrováním Microsoft 365. Stává se to při prvním přihlášení k Microsoft 365. Chcete-li tento problém vyřešit, vyberte **Zpět** ve svém prohlížeči pro návrat na předchozí stránku.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>Rozumím, jak upravit šablonu pomocí Microsoft 365 v první relaci aplikace a jak používat šablonu v druhé relaci aplikace upravením šablony tak, abych mohl vidět, jaký vliv mají změny na vygenerovaný obchodní dokument. Mohu používat desktopovou aplikaci Office stejným způsobem?

Ano, můžete. V první relaci aplikace vyberte možnost **Otevřít v desktopové aplikaci**. Šablona bude uložena do dočasného úložiště souborů a bude otevřena v desktopové aplikaci Office. Nyní, když chcete-zobrazit náhled změn šablony ve vygenerovaném obchodním dokumentu, proveďte následující kroky:

1. Upravte šablonu pomocí desktopové aplikace Office.
2. Vyberte možnost **Uložit** v desktopové aplikaci Office.
3. Na stránce **Editor šablon BDM** v první relaci aplikace vyberte možnost **Synchronizovat uloženou kopii**.
4. Spusťte tento formát šablony elektronického výkaznictví v druhé relaci aplikace.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Když vyberu Otevřít v desktopové aplikaci, zobrazí se následující chybová zpráva: „Hodnota nemůže být null. Název parametru: externalId. " Jak lze tento problém vyřešit?

Pravděpodobně jste se přihlásili k aktuální instanci aplikace v doméně Azure AD, která se liší od domény Azure AD, která byla použita pro nasazení této instance. Vzhledem k tomu, že služba SharePoint, která slouží k ukládání šablon pro jejich zpřístupnění pro úpravy pomocí desktopových aplikací Office, patří do stejné domény, nemáme žádná oprávnění pro přístup ke službě SharePoint. Chcete-li tento problém vyřešit, přihlaste se k aktuální instanci s použitím přihlašovacích údajů uživatele se správnou doménou Azure AD.

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu OPENXML (listopad 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu Word](tasks/er-design-configuration-word-2016-11.md)

[Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md)

[Konfigurace elektronického výkaznictví pro doplňování dat do Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>Seznam konfigurací ER, které byly vydány v aplikaci Finance na podporu konfigurovatelných obchodních dokumentů

[Seznam](general-electronic-reporting.md#list-of-configurations) konfigurací ER pro Finance se neustále aktualizuje. Otevřete [Globální úložiště](er-download-configurations-global-repo.md) ke kontrole seznamu konfigurací ER, které jsou aktuálně podporovány. Můžete [filtrovat](../../../finance/localizations/enhanced-filtering-global-repo.md) globální úložiště pro kontrolu seznamu konfigurací ER, které se používají k podpoře konfigurovatelných obchodních dokumentů.

![Filtrování obsahu globálního úložiště na stránce úložiště konfigurace](./media/bdm-overview-filterglobalrepo.gif)

V následující tabulce je uveden seznam konfigurací ER, které podporují konfigurovatelné obchodní dokumenty a které byly vydány v modulu Finance do prosince 2020.

| Konfigurace datového modelu    | Konfigurace formátu                           |
|-----------------------------|-------------------------------------------------|
| Model přepravní doklad        | Přepravní doklad (Excel)                          |
|                             | Přepravní doklad (Word)                           |
| Model certifikátu o původu | Certifikát o původu (Excel)                   |
|                             | Certifikát o původu (Word)                    |
| Model faktury               | Dobropis a vrubopis zákazníka (Excel)          |
|                             | Dobropis a vrubopis zákazníka (Word)           |
|                             | Volná textová faktura (Excel)                       |
|                             | Volná textová faktura (Excel) (BH)                  |
|                             | Volná textová faktura (FR) (Excel)                  |
|                             | Volná textová faktura (LT) (Excel)                  |
|                             | Volná textová faktura (LV) (Excel)                  |
|                             | Volná textová faktura (PL) (Excel)                  |
|                             | Volná textová faktura (CZ) (Excel)                  |
|                             | Volná textová faktura (EE) (Excel)                  |
|                             | Volná textová faktura (HU) (Excel)                  |
|                             | Volná textová faktura (TH) (Excel)                  |
|                             | Volná textová faktura (Word)                        |
|                             | Řádkové položky smlouvy na projekt (Excel)             |
|                             | Řádkové položky smlouvy na projekt (CZ) (Excel)        |
|                             | Řádkové položky smlouvy na projekt (Excel) (BH)        |
|                             | Řádkové položky smlouvy na projekt (HU) (Excel)        |
|                             | Řádkové položky smlouvy na projekt (LT) (Excel)        |
|                             | Řádkové položky smlouvy na projekt (PL) (Excel)        |
|                             | Řádkové položky smlouvy na projekt (Word)              |
|                             | Vydání uchování zákazníka projektu (Excel)      |
|                             | Vydání uchování zákazníka projektu (CZ) (Excel) |
|                             | Vydání uchování zákazníka projektu (HU) (Excel) |
|                             | Vydání uchování zákazníka projektu (LT) (Excel) |
|                             | Vydání uchování zákazníka projektu (PL) (Excel) |
|                             | Vydání uchování zákazníka projektu (TH) (Excel) |
|                             | Vydání uchování zákazníka projektu (Word)       |
|                             | Projektová faktura (Excel)                         |
|                             | Projektová faktura (Word)                          |
|                             | Projektová faktura (AE) (Excel)                    |
|                             | Projektová faktura (CZ) (Excel)                    |
|                             | Projektová faktura (Excel) (BH)                    |
|                             | Projektová faktura (HU) (Excel)                    |
|                             | Projektová faktura (JP) (Excel)                    |
|                             | Projektová faktura (LT) (Excel)                    |
|                             | Projektová faktura (PL) (Excel)                    |
|                             | Projektová faktura (TH) (Excel)                    |
|                             | Projektová faktura (MY) (Excel)               |
|                             | Jednoduchá projektová faktura (MY) (Excel)             |
|                             | Faktura pro správu projektu (Excel)                  |
|                             | Faktura pro správu projektu (CZ) (Excel)             |
|                             | Faktura pro správu projektu (Excel) (BH)             |
|                             | Faktura pro správu projektu (HU) (Excel)             |
|                             | Faktura pro správu projektu (JP) (Excel)             |
|                             | Faktura pro správu projektu (LT) (Excel)             |
|                             | Faktura pro správu projektu (PL) (Excel)             |
|                             | Faktura pro správu projektu (Word)                   |
|                             | Zálohová nákupní faktura (Excel)                |
|                             | Zálohová nákupní faktura (Word)                 |
|                             | Prodejní zálohová faktura (Excel)                   |
|                             | Prodejní zálohová faktura (Word)                    |
|                             | Prodejní zálohová faktura (PL) (Excel)              |
|                             | Prodejní faktura (Excel)                           |
|                             | Prodejní faktura (Excel) (BH)                      |
|                             | Prodejní faktura (Excel) (CZ)                      |
|                             | Prodejní faktura (Excel) (EE)                      |
|                             | Prodejní faktura (Excel) (FR)                      |
|                             | Prodejní faktura (Excel) (HU)                      |
|                             | Prodejní faktura (Excel) (IN)                      |
|                             | Prodejní faktura (Excel) (LT)                      |
|                             | Prodejní faktura (Excel) (LV)                      |
|                             | Prodejní faktura (Excel) (PL)                      |
|                             | Prodejní faktura (Excel) (TH)                      |
|                             | Prodejní faktura (Word)                            |
|                             | Obchodní faktura TMS (Excel)                  |
|                             | Obchodní faktura TMS (Word)                   |
|                             | Příloha dokumentu faktury dodavatele (Excel)                 |
|                             | Příloha dokumentu faktury dodavatele (CZ) (Excel)            |
|                             | Příloha dokumentu faktury dodavatele (HU) (Excel)            |
|                             | Příloha dokumentu faktury dodavatele (IN) (Excel)            |
|                             | Příloha dokumentu faktury dodavatele (LT) (Excel)            |
|                             | Příloha dokumentu faktury dodavatele (LV) (Excel)            |
|                             | Příloha dokumentu faktury dodavatele (MY) (Excel)            |
|                             | Příloha dokumentu faktury dodavatele (Word)                  |
| Model objednávky                 | Potvrzení smlouvy (Excel)                  |
|                             | Potvrzení smlouvy (Word)                   |
|                             | Potvrzení nákupní smlouvy (Excel)         |
|                             | Potvrzení nákupní smlouvy (Word)          |
|                             | Nákupní objednávka (Excel)                          |
|                             | Nákupní objednávka (CZ) (Excel)                     |
|                             | Dotaz na nákupní objednávku (CZ) (Excel)             |
|                             | Nákupní objednávka (HU) (Excel)                     |
|                             | Dotaz na nákupní objednávku (HU) (Excel)             |
|                             | Řádek nákupní objednávka (Word)                           |
|                             | Dotaz na nákupní objednávku (Excel)                  |
|                             | Dotaz na nákupní objednávku (Word)                   |
|                             | Potvrzení prodejní objednávky (Excel)                |
|                             | Potvrzení prodejní objednávky (CZ) (Excel)           |
|                             | Potvrzení prodejní objednávky (HU) (Excel)           |
|                             | Potvrzení prodejní objednávky (Word)                 |
| Model balení          | Obsah kontejneru (Excel)                      |
|                             | Obsah kontejneru (Word)                       |
|                             | Seznam nakládky (Excel)                               |
|                             | Seznam nakládky (Word)                                |
|                             | Výběrový seznam (Excel)                            |
|                             | Výběrový seznam (CZ) (Excel)                       |
|                             | Výdejka (Word)                             |
|                             | Výběrový seznam produkce (Excel)                    |
|                             | Výběrový seznam produkce (Word)                     |
|                             | Výběrový seznam zásilky pro načtení (Excel)             |
|                             | Výběrový seznam zásilky pro načtení (Word)              |
|                             | Výběrový seznam pro zásilku (Excel)         |
|                             | Výběrový seznam pro zásilku (Word)          |
|                             | Výběrový seznam zásilky pro vlnu (Excel)             |
|                             | Výběrový seznam zásilky pro vlnu (Word)              |
| Model platby               | Poradenství ohledně plateb zákazníkům (Excel)                 |
|                             | Poradenství ohledně plateb zákazníkům (Word)                  |
|                             | Poradenství ohledně plateb dodavatelům (Excel)                   |
|                             | Poradenství ohledně plateb dodavatelům (Word)                    |
| Model nabídky             | Nabídka projektu (Excel)                       |
|                             | Nabídky projektu (Word)                        |
|                             | Řádky požadavku na nabídku (Excel)                   |
|                             | Řádky požadavku na nabídku (Přijetí) (Excel)          |
|                             | Řádky požadavku na nabídku (Přijetí) (Word)           |
|                             | Řádky požadavku na nabídku (Odmítnutí) (Excel)          |
|                             | Řádky požadavku na nabídku (Odmítnutí) (Word)           |
|                             | Požadavek na nabídku (Vrácení) (Excel)          |
|                             | Požadavek na nabídku (Vrácení) (Word)           |
|                             | Požadavek na nabídku (Word)                    |
|                             | Prodejní nabídka (Excel)                         |
|                             | Prodejní nabídka (CZ) (Excel)                    |
|                             | Prodejní nabídka (HU) (Excel)                    |
|                             | Řádek nabídky (Word)                          |
|                             | Potvrzení prodejní nabídky (Excel)            |
|                             | Potvrzení prodejní nabídky (Word)             |
| Model odsouhlasení        | Výpis z běžného účtu, Ext (Excel)             |
|                             | Výpis z běžného účtu, Ext (CN) (Excel)        |
|                             | Výpis z běžného účtu, Ext (Word)              |
|                             | Výpis z běžného účtu, Francie (Excel)          |
| Model připomenutí              | Upomínka inkasa (Excel)                  |
|                             | Upomínka inkasa (CN) (Excel)             |
|                             | Upomínka (Word)                   |
|                             | Oznámení úroků odběratele (Excel)                  |
|                             | Oznámení úroků odběratele (Word)                   |
| Model nákladního listu               | Načíst nabídku (Excel)                             |
|                             | Načíst nabídku (Word)                              |
|                             | Nákupní objednávka – dodací list (Excel)             |
|                             | Nákupní objednávka – dodací list (CZ) (Excel)        |
|                             | Nákupní objednávka – dodací list (Word)              |
|                             | Trasa (Excel)                                   |
|                             | Trasa (Word)                                    |
|                             | Prodejní objednávka – dodací list (Excel)                |
|                             | Prodejní objednávka – dodací list (CZ) (Excel)           |
|                             | Prodejní objednávka – dodací list (LT) (Excel)           |
|                             | Prodejní objednávka – dodací list (PL) (Excel)           |
|                             | Prodejní objednávka – dodací list (Word)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
