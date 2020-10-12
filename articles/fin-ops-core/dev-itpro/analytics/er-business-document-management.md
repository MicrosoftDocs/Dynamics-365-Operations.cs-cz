---
title: Přehled správy obchodních dokumentů
description: Toto téma obsahuje informace o použití funkce správy obchodních dokumentů v rámci architektury elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65874e5ca73c18c3df7b94b8abb6eb15491482bf
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893128"
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

## <a name="business-document-availability"></a>Dostupnost obchodních dokumentů

Při vydání veřejné verze Preview budou k dispozici následující sestavy s šablonami založeným na aplikaci Excel:

**Pohledávky** (srpen 2019)

- Prodejní zálohová faktura
- Prodejní objednávka – dodací list

**Závazky** (srpen 2019)

- Zálohová nákupní faktura
- Nákupní objednávka
- Nákupní objednávka – dodací list

Budou k dispozici další sestavy. Zvláštní oznámení o dalších sestavách budou odeslána samostatně. 

Úplný seznam všech sestav plánovaných pro vydání v říjnu 2019 lze najít v části [Konfigurovatelné vykazování obchodních dokumentů v aplikacích Word a Excel](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details). Chcete-li získat další informace o této funkci, vyplňte příklad tomto tématu.

## <a name="configure-er-parameters"></a>Konfigurace parametrů ER

Vzhledem k tomu, že správa obchodních dokumentů je na vrcholu architektury elektronického výkaznictví, je nutné parametry elektronického výkaznictví nakonfigurovat tak, aby začaly spolupracovat se správou obchodních dokumentů. Nejprve je třeba nastavit parametry elektronického výkaznictví, jak je popsáno v tématu [Konfigurace architektury elektronického výkaznictví (ER)](electronic-reporting-er-configure-parameters.md). Je také nutné přidat nového poskytovatele konfigurace, jak je popsáno v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Pracovní prostor elektronického výkaznictví](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Import řešení elektronického výkaznictví

V příkladu tohoto postupu jsou použity ukázkové konfigurace ER. Do aktuální instance aplikace Dynamics 365 Finance je nutné importovat konfigurace ER obsahující šablony obchodních dokumentů, které lze upravit pomocí správy obchodních dokumentů. Chcete-li provést tento postup, stáhněte a uložte následující soubory.

**Ukázka fakturačního řešení elektronického výkaznictví pro zákazníky**

| **Soubor**                                  | **Obsah**                                |
|-------------------------------------------|--------------------------------------------|
| Customer invoicing model.version.2.xml    | [Konfigurace datového modelu elektronického výkaznictví](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [Konfigurace formátu elektronického výkaznictví volné faktury](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Ukázka řešení platebních šeků elektronického výkaznictví**

| **Soubor**                                  | **Obsah**                                |
|-------------------------------------------|--------------------------------------------|
| Model for cheques.version.10.xml          | [Konfigurace datového modelu elektronického výkaznictví](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml  | [Konfigurace formátu elektronického výkaznictví platebního šeku](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Ukázka řešení zahraničního obchodu elektronického výkaznictví**

| **Soubor**                                  | **Obsah**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat model.version.1.xml             | [Konfigurace datového modelu elektronického výkaznictví](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml          | [Konfigurace formátu elektronického výkaznictví sestavy řízení systému Intrastat](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

K importu každého souboru použijte následující postup. Před importem odpovídající *konfigurace* elektronického výkaznictví importujte pro jednotlivá řešení elektronického výkaznictví konfiguraci *datového modelu* elektronického výkaznictví v tabulkách výše.

1. Otevřete stránku **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. V horní části stránky vyberte možnost **Směna**.
3. Vyberte **Načíst ze souboru XML**.
4. Výběrem možnosti **Procházet** načtete požadovaný soubor XML.
5. Kliknutím na tlačítko **OK** potvrďte import konfigurace.

![Stránka konfigurací elektronického výkaznictví](./media/BDM-Overview-ERSolutions.png)


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

>[!NOTE]
> Další informace o použití nového uživatelského rozhraní dokumentu v modulu Správa obchodních dokumentů naleznete v tématu [Nové uživatelské rozhraní dokumentů v modulu Správa obchodních dokumentů](er-business-document-management-new-template-ui.md).

![Pracovní prostor Správa funkcí](./media/BDM-Overview-FMEnabling.png)

Další informace o aktivaci nových funkcí naleznete v tématu [Přehled správy funkcí](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Konfigurace parametrů

Chcete-li nastavit základní parametry pro správu obchodních dokumentů, použijte informace v následujících sekcích.

### <a name="prerequisites-for-parameter-setup"></a>Předpoklady pro nastavení parametrů
Před nastavením správy obchodních dokumentů je nutné nastavit v architektuře správy dokumentů požadovaný typ dokumentu. Tento typ dokumentu se používá k určení dočasného úložiště dokumentů ve formátech Office (Excel a Word), které se používají jako šablony pro sestavy elektronického výkaznictví. Dočasné šablony úložiště lze upravit pomocí desktopových aplikací Office.

Pro tento typ dokumentu je nutné vybrat následující hodnoty atributů.

| **Název atributu**  | **Hodnota atributu**   |
|---------------------|-----------------------|
| Třída               | Připojit soubor           |
| Seskupit               | Soubor                  |
| Umístění            | SharePoint            |

Informace o nastavení požadovaných parametrů správy dokumentů a typů dokumentů naleznete v tématu [Konfigurace správy dokumentů](../../fin-ops/organization-administration/configure-document-management.md).

![Nastavení typu dokumentu pro správu dokumentů](./media/BDM-Overview-DMSetting.png)

### <a name=""></a><a name="SetupBdmParameters">Nastavení parametrů</a>

Na stránce **parametry obchodního dokumentu** lze nastavit základní parametry správy obchodních dokumentů. Na stránku mohou přistupovat jen někteří uživatelé. Mezi ně patří:

- Uživatelé s rolí **Správce systému**.
- Uživatelé s libovolnou rolí s oprávněním **Údržba parametrů správy obchodních dokumentů** (název AOT **ERBDMaintainParameters**).

Pomocí následujícího postupu nastavíte základní parametry pro všechny právnické osoby.

1. Přihlaste se jako uživatel s přístupem na stránku **Parametry obchodního dokumentu**.
2. Přejděte do části **Správa organizace** \> **Elektronické vykazování** \> **Správu obchodních dokumentů** \> **Parametry obchodního dokumentu**.
3.    Na stránce **Parametry obchodního dokumentu** na kartě **Přílohy** v poli **Typ dokumentu SharePoint** definujte typ dokumentu, který se má použít k dočasnému uložení šablon ve formátech Office v době, kdy jsou upravovat pomocí desktopových aplikací Office. 

> [!NOTE]
> Pro tento parametr jsou k dispozici pouze typy dokumentů, které jsou konfigurovány s použitím umístění SharePoint.

![Nastavení parametrů správy obchodních dokumentů](./media/BDM-Overview-BDMSetting.png)

Vybraný typ dokumentu je specifický pro společnost a bude použit, pokud uživatel pracuje se správou obchodních dokumentů ve společnosti, pro kterou je nastaven vybraný typ dokumentu. Pokud uživatel pracuje se správou obchodních dokumentů v jiné společnosti, bude použit stejný vybraný typ dokumentu, pokud nebyl pro tuto společnost konfigurován jiný. Pokud byl typ dokumentu konfigurován, bude použit namísto typu vybraného v poli **Typ dokumentu SharePoint**.

> [!NOTE]
> Parametr **Typ dokumentu SharePoint** definuje složku SharePoint jako dočasné úložiště pro šablony, které lze upravovat pomocí aplikací Microsoft Excel nebo Word. Tento parametr je nutné nastavit, pokud chcete používat tyto desktopové aplikace Office pro úpravy šablon. Další informace naleznete v tématu [Úprava šablony v desktopové aplikaci Office](#EditInOfficeDesktopApp). Chcete-li upravit šablonu pouze pomocí funkce v aplikaci Microsoft 365, můžete tento parametr ponechat prázdný. Další informace naleznete v tématu [Úprava šablony v Microsoft 365](#EditInOffice365).

## <a name="configure-access-permissions"></a>Konfigurace přístupových oprávnění

Ve výchozím nastavení, pokud není povolen přístup k oprávněním pro správu obchodních dokumentů, uvidí každý uživatel s přístupem k pracovnímu prostoru správy obchodních dokumentů všechny šablony řešení elektronického výkaznictví, které jsou k dispozici. Pracovní prostor správy obchodních dokumentů zobrazí pouze ty šablony, které se nacházejí v konfiguracích formátu elektronického výkaznictví a jsou označeny značkou **Typ obchodního dokumentu**.

![Stránka konfigurací elektronického výkaznictví](./media/BDM-Overview-ERFormatTags.png)

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

    ![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-TemplatesForAlice1.png)

3. Na stránce **Konfigurátor přístupových oprávnění** vyberte možnost **Nastavení oprávnění přístupu**.
4. V dialogovém okně **Nastavení přístupových oprávnění pro úpravy šablon** povolte možnost **Použít konfigurovaná přístupová oprávnění**.
5. Klepnutím na tlačítko **OK** potvrďte, že byla povolena oprávnění přístupu ke správě obchodních dokumentů.

    ![Stránka s konfigurací přístupových oprávnění ke správě obchodních dokumentů](./media/BDM-Overview-TemplatesAccess2.png)

6. Chcete-li zadat novou obchodní roli, pro kterou mají být konfigurována oprávnění pro přístup k šablonám správy obchodních dokumentů, vyberte možnost **Přidat**.
7. V dialogovém okně **Role zabezpečení** vyberte roli **Úředník pohledávek** a poté klepnutím na tlačítko **OK** potvrďte výběr role.
8. Na kartě **Přístupová oprávnění dle značek konfigurací** vyberte možnost **Nové**.
9. V poli **Typ značky** vyberte možnost **Funkční oblast** a v poli **ID** vyberte možnost **Fakturace**.
10. Chcete-li uložit konfigurovaná přístupová oprávnění pro vybranou roli, vyberte možnost **Uložit**.

    Aktuální nastavení znamená, že pro každého uživatele, který má roli **Úředník pohledávek** a funkční oprávnění **Správa šablon obchodních dokumentů** (název AOT **ERBDManageTemplates**), šablony konfigurací elektronického výkaznictví, které mají hodnotu **Fakturace** pro značku **Funkční oblast**, budou k dispozici pro úpravy v pracovním prostoru Správa obchodních dokumentů.

11. Přepněte podokno **Související informace** z pravé strany aktuální stránky. V podokně **Související informace** je zobrazen způsob použití konfigurovaných přístupových oprávnění včetně informací o tom, jaké konfigurační šablony elektronického výkaznictví budou k dispozici pro uživatele s rolí **Úředník pohledávek**.

    ![Stránka s konfigurací přístupových oprávnění ke správě obchodních dokumentů](./media/BDM-Overview-TemplatesAccess3.png)

12. Na kartě **Přístupová oprávnění dle konfigurací** vyberte možnost **Přidat**.
13. V dialogovém **Výběr konfigurace** označte konfiguraci formátu elektronického výkaznictví jako **Sestavu Intrastat**.
14. Kliknutím na tlačítko **OK** potvrďte zadání vybraných konfigurací a výběrem možnosti **Uložit** uložte konfigurovaná přístupová oprávnění pro vybranou roli.

Aktuální nastavení znamená, že pro každého uživatele, který má roli **Úředník pohledávek** a funkční oprávnění **Správa šablon obchodních dokumentů** (název AOT **ERBDManageTemplates**), následující šablony budou k dispozici pro úpravy v pracovním prostoru Správa obchodních dokumentů:

- Šablony, které mají hodnotu **Fakturace** pro značku **Funkční oblast**.
- Šablony z konfigurací formátu elektronického výkaznictví, které jsou uvedeny na kartě **Přístupová oprávnění dle konfigurací** (šablony z konfigurace formátu **Sestava Intrastat** domény **Statutární vykazování** v tomto příkladu).

![Stránka s konfigurací přístupových oprávnění ke správě obchodních dokumentů](./media/BDM-Overview-TemplatesAccess4.png)

Následující obrázek zobrazuje, co pracovní prostor Správa obchodních dokumentů umožňuje uživateli s rolí **Úředník pohledávek**. S aktuálním nastavením přístupového oprávnění ke správě obchodních dokumentů může uživatel upravovat šablony obchodních dokumentů z domény **Fakturace** a z konfigurace formátu elektronického výkaznictví **Sestava Intrastat**. Šablony z domény **Platby** nejsou přístupné pro roli **Úředník pohledávek**.

![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-TemplatesForAlice2.png)

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

![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingTemplate1.png)

Na kartě **Šablony** se zobrazí obsah vybrané šablony. Vyberte kartu **Podrobnosti**, na které si můžete prohlédnout podrobnosti o vybrané šabloně a podrobnosti o konfiguraci formátu elektronického výkaznictví, kde je tato šablona umístěna. Všimněte si, že všechny šablony mají stav **Publikováno**a neobsahují údaje ve sloupci **Revize**. To znamená, že tyto šablony aktuálně nejsou upravovány.

Pokud je funkce **Prostředí UI podobné systému Office pro správu obchodního dokumentu** zapnuta v pracovním prostoru **Správa funkcí**, hlavní mřížka v pracovním prostoru **Správa obchodních dokumentů** zobrazuje šablony, které jsou vlastněny vaším poskytovatelem konfigurace ER (tj. poskytovatelem, který je aktuálně označen jako aktivní v pracovním prostoru **Elektronického vykazování**). Po vybrání jedné z těchto šablon můžete vybrat možnost **Upravit šablonu** a začít ji upravovat.

Chcete-li pracovat se šablonami, které jsou vlastněny jinými zprostředkovateli konfigurace ER, vyberte možnost **Nový dokument** a vytvořte kopii šablony, která je vlastněna vaším poskytovatelem ER. Poté můžete začít upravovat kopii. Další informace naleznete v tématu [Nové uživatelské rozhraní dokumentu v modulu Správa obchodních dokumentů](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Zahájení úprav šablon vlastněných vaším poskytovatelem konfigurace

1. V pracovním prostoru Správa obchodních dokumentů vyberte v seznamu šablonu **Formát tisku šeků**.
2. Zvolte kartu **Podrobnosti**.

![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingTemplate2.png)

Pro vybranou šablonu je k dispozici možnost **Upravit šablonu**. Tato možnost je vždy k dispozici pro šablonu v konfiguraci formátu elektronického výkaznictví, která je vlastněna aktivním poskytovatelem konfigurace elektronického výkaznictví (v tomto případě **Litware, Inc.**). Je -li vybrána možnost **Upravit šablonu**, budete moci upravit existující šablonu z verze konceptu základní konfigurace formátu elektronického výkaznictví.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Zahájení úprav šablon vlastněných ostatními poskytovateli

1. V pracovním prostoru správy obchodních dokumentů vyberte dokument, který chcete použít jako šablonu.

![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingTemplate3.png)

3. Vyberte **Nový dokument** a v poli **Název** změňte v případě potřeby název upravitelné šablony. Text se použije k pojmenování konfigurace formátu elektronického výkaznictví, která je automaticky vytvořena. Všimněte si, že verze konceptu této konfigurace **(Kopie sestavy FTI odběratele (GER)kopie**), která bude obsahovat upravenou šablonu, bude automaticky označena pro spuštění tohoto formátu elektronického výkaznictví pro aktuálního uživatele. Zároveň bude původní neupravená šablona ze základní konfigurace formátu elektronického výkaznictví použita ke spuštění tohoto formátu elektronického výkaznictví pro libovolného jiného uživatele.
4. V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.
5. V poli **Komentář** změňte komentář pro automaticky vytvořenou revizi upravitelné šablony.
6. Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav

![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingTemplate4.png)

Možnost **Nový dokument** je vždy k dispozici pro šablonu v konfiguraci formátu elektronického výkaznictví poskytovanou aktuálním a jiným poskytovatelem (v tomto případě Microsoft), který nemá žádnou revizi. Upravená šablona bude poté uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.

### <a name="start-editing-a-template"></a>Zahájení úpravy šablony

1. Z vybrané šablony vyberte možnost **Upravit dokument**.
2. V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.
3. V poli **Komentář** změňte poznámku pro automaticky vytvořenou revizi upravitelné šablony.

    ![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingTemplate5.png)

5. Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.

Otevře se stránka **Editor šablony BDM**. Vybraná šablona bude k dispozici pro online úpravy pomocí Microsoft 365.

![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingLayout1.png)

### <a name=""></a><a name="EditInOffice365">Úprava šablony pomocí Microsoft 365</a>

Šablonu můžete upravit pomocí aplikace Microsoft 365. Například v řešení Office Online změníte písmo výzev polí v záhlaví šablony z **Obyčejné** na **Tučné**. Tyto změny se automaticky uloží v upravitelné šabloně, která se nachází v úložišti primární šablony (standardně úložiště objektu blob služby Azure). To je konfigurováno pro rámec elektronického výkaznictví.

![Stránka editoru šablon pro správu obchodních dokumentů](./media/BDM-Overview-EditingLayout2.png)

### <a name=""></a><a name="EditInOfficeDesktopApp">Úprava šablony v desktopové aplikaci Office</a>

> [!NOTE]
> Tato funkce je k dispozici pouze tehdy, když je parametr **Typ dokumentu SharePoint** správně nakonfigurován. Další informace naleznete v tématu [Konfigurace parametrů](#SetupBdmParameters).

1. Chcete- li upravit šablonu pomocí funkce desktopové aplikace Office (v tomto příkladu aplikace Excel), vyberte možnost **Otevřít v desktopové aplikaci**. Upravitelná šablona je zkopírována z trvalého úložiště do dočasného úložiště konfigurovaného v parametrech správy obchodních dokumentů jako složka SharePoint.
2. Potvrďte, že chcete otevřít šablonu z dočasného úložiště souborů v desktopové aplikaci Office Excel.

    ![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingLayout3.png)

3. Upravte šablonu. Například změňte barvu písma výzev polí v záhlaví šablony z **Černá** na **Modrá**.

    ![Stránka editoru šablon pro správu obchodních dokumentů](./media/BDM-Overview-EditingLayout4.png)

4. Volbou **Uložit** v desktopové aplikaci Excel uložte změny šablony do dočasného úložiště.

    ![Stránka editoru šablon pro správu obchodních dokumentů](./media/BDM-Overview-EditingLayout5.png)

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

![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Test upravené šablony 

1. V aplikaci změňte položku na společnost **USMF**.
2. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
3. Vyberte fakturu **FTI-00000002** a poté vyberte možnost **Správatisku**.
4. Chcete-li určit rozsah faktur, které mají být zpracovány, vyberte **Modul – Pohledávky** \> **Dokumenty** \> **Volná faktura** \> **Původní dokument**.
5. V poli **Formát sestavy** vyberte formát elektronického výkaznictví **Kopie sestavy FTI odběratele (GER)** pro zadanou úroveň dokumentu.

    ![Stránka nastavení správy tisku](./media/BDM-Overview-TestRun1.png)

6. Stisknutím klávesy **Escape** zavřete aktuální stránku.
7. Vyberte možnost **Tisk** a poté klepněte namožnost **Vybráno**.
8. Stáhněte dokument a otevřete jej pomocí desktopové aplikace Excel.

![Stránka Volné faktury](./media/BDM-Overview-TestRun2.png)

Upravená šablona slouží k vygenerování sestavy volné faktury pro vybranou položku. Chcete-li analyzovat, jak je tato sestava ovlivněna změnami, které jste provedli v šabloně, můžete tuto sestavu spustit v jedné relaci aplikace přímo po změně šablony v jiné relaci aplikace.

### <a name="create-an-alternative-template-revision"></a>Vytvoření alternativní revize šablony

1. Otevřete stránku **Editor šablon BDM** a vyberte šablonu **Kopie šablony FTI odběratele (GER)**.
2. Na kartě **Revize** vyberte možnost **Nová**.
3. V případě potřeby změňte v poli **Název** název druhé revize a založte jej na aktuálně aktivní první revizi.
4. Pokud je třeba, v poli **Komentář** změňte poznámku pro automaticky vytvořenou revizi upravitelné šablony.

    ![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-AddRevision.png)

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

![Stránka pracovního prostoru správy obchodních dokumentů](./media/BDM-Overview-RevokeChanges.png)

1. Na stránce **Editor šablon BDM** vyberte kartu **Šablona**.
2. Vyberte možnost **Zpět**.
3. Pokud vyberete možnost **OK** k odvolání změn provedených v šabloně, upravená šablona bude nahrazena původní šablonou a všechny změny budou odebrány. Pokud odvoláte změny šablony, budete moci šablonu odstranit. Chcete-li prozkoumat ostatní možnosti, vyberte možnost **Storno**.

### <a name="publish-a-modified-template"></a>Publikování upravené šablony
1. Na stránce **Editor šablon BDM** na kartě **Šablona** vyberte **Publikovat**.
2. Vyberete-li možnost **OK** pro potvrzení publikování, draft odvozeného formátu elektronického výkaznictví **Kopie sestavy FTI odběratele (GER)**, který obsahuje upravenou šablonu, bude označen jako dokončený. Upravená šablona bude k dispozici pro ostatní uživatele. Dokončené verze tohoto formátu elektronického výkaznictví zachovají pouze poslední aktivní revizi vaší šablony. Ostatní revize budou odstraněny. Chcete-li prozkoumat ostatní možnosti, vyberte možnost **Storno**.

## <a name="frequently-asked-questions"></a>Časté dotazy

#### <a name="i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page"></a>Vybral jsem možnost **Upravit dokument**, ale namísto otevření stránky **Editor šablon BDM** v aplikaci Finance and Operations jsem byl přesměrován na webovou stránku Microsoft 365.
Jedná se o známý problém s přesměrováním Microsoft 365. To se stává při prvním přihlášení k Microsoft 365. Chcete-li tento problém vyřešit, v prohlížeči vyberte tlačítko **Zpět**, čímž přejdete zpět.

#### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>Rozumím, jak upravit šablonu pomocí Microsoft 365 v první relaci aplikace a jak používat šablonu v druhé relaci aplikace upravením šablony tak, abych mohl vidět, jaký vliv mají změny na vygenerovaný obchodní dokument. Mohu to provést pomocí desktopové aplikace Office?
Ano, můžete. V první relaci aplikace vyberte možnost **Otevřít v desktopové aplikaci**. Šablona bude uložena do dočasného úložiště souborů a bude otevřena v desktopové aplikaci Office. Nyní, když chcete-zobrazit náhled změn šablony ve vygenerovaném obchodním dokumentu, proveďte následující kroky:

1. Upravte šablonu pomocí desktopové aplikace Office.
2. Vyberte možnost **Uložit** v desktopové aplikaci Office.
3. Na stránce **Editor šablon BDM** v první relaci aplikace vyberte možnost **Synchronizovat uloženou kopii**.
4. Spusťte tento formát šablony elektronického výkaznictví v druhé relaci aplikace.

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>Zobrazuje se mi chyba „Hodnota musí být zadána. Název parametru: externalId“ při výběru možnosti **Otevřít v desktopové aplikaci**. Jak lze tento problém vyřešit? 
Pravděpodobně jste se přihlásili k aktuální instanci aplikace v doméně Azure AD, která se liší od domény Azure AD, která byla použita pro nasazení této instance. Vzhledem k tomu, že služba SharePoint, která slouží k ukládání šablon pro jejich zpřístupnění pro úpravy pomocí desktopových aplikací Office, patří do stejné domény, nemáme žádná oprávnění pro přístup ke službě SharePoint. Chcete-li tento problém vyřešit, přihlaste se k aktuální instanci s použitím přihlašovacích údajů uživatele se správnou doménou Azure AD.

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu OPENXML (listopad 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu Word](tasks/er-design-configuration-word-2016-11.md)

[Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](electronic-reporting-embed-images-shapes.md)

[Konfigurace elektronického výkaznictví pro doplňování dat do Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)

