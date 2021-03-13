---
title: Vytvoření aplikace pro export opakujících se dat
description: Tento článek ukazuje, jak vytvořit logic app v Microsoft Azure, která exportuje data z Microsoft Dynamics 365 Human Resources na opakujícím se plánu.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 97972d2179c42e9d2d672cbebb75643ef0a02a62
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111756"
---
# <a name="create-a-recurring-data-export-app"></a>Vytvoření aplikace pro export opakujících se dat

Tento článek ukazuje, jak vytvořit logic app v Microsoft Azure, která exportuje data z Microsoft Dynamics 365 Human Resources na opakujícím se plánu. Výukový kurz využívá pro export dat rozhraní API REST balíčku DMF aplikace Human Resources. Po exportu dat uloží logic app exportovaný balíček dat do složky Microsoft OneDrive pro firmy.

## <a name="business-scenario"></a>Scénáře obchodu

V jednom typickém obchodním scénáři pro integrace Microsoft Dynamics 365 je nutné data exportovat do podrřízeného systému v opakovaném plánu. Tento výukový program ukazuje, jak exportovat všechny záznamy pracovníka z Microsoft Dynamics 365 Human Resources a uložit seznam pracovníků do složky OneDrive pro firmy.

> [!TIP]
> Konkrétní data, která jsou exportována v tomto kurzu a cíl exportovaných dat, jsou pouze příklady. Lze je snadno změnit tak, aby splňovaly vaše obchodní potřeby.

## <a name="technologies-used"></a>Použité technologie

Tento výukový kurz používá následující technologie:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – Hlavní zdroj dat pro pracovníky, kteří budou exportováni.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – technologie, která poskytuje orchestraci a plánování opakovaného exportu.

    - **[Konektory](https://docs.microsoft.com/azure/connectors/apis-list)** – technologie, která se používá k propojení logic app s požadovanými koncovými body.

        - Konektor [HTTP s Azure AD](https://docs.microsoft.com/connectors/webcontents/)
        - Konektor [OneDrive pro firmy](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)

- **[Rozhraní REST API balíčku DMF](../dev-itpro/data-entities/data-management-api.md)** – technologie, která slouží k aktivaci exportu a sledování jejího průběhu.
- **[OneDrive pro firmy](https://onedrive.live.com/about/business/)** – cíl pro exportované pracovníky.

## <a name="prerequisites"></a>Předpoklady

Před zahájením cvičení v tomto kurzu je nutné mít k dispozici následující položky:

- Prostředí Human Resources, které má oprávnění na úrovni správce v daném prostředí
- [Předplatné Azure](https://azure.microsoft.com/free/) pro hostování logic app

## <a name="the-exercise"></a>Cvičení

Na konci tohoto cvičení budete mít logic app, která je připojena k prostředí Human Resources a ke svému účtu OneDrive pro firmy. Logic app exportuje balíček dat z Human Resources, počká na dokončení exportu, stáhne exportovaný balíček dat a uloží jej do složky OneDrive pro firmy, kterou jste určili.

Dokončená logic app se bude podobat následující ilustraci.

![Přehled logic app](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>Krok 1: Vytvoření projektu exportu dat v Human Resources

V aplikaci Human Resources vytvořte projekt exportu dat, který exportuje pracovníky. Nazvěte projekt **Export pracovníků** a ujistěte se, že je možnost **Generovat balíček dat** nastaven na **Ano**. Přidejte do projektu jednu entitu (**Pracovník**) a vyberte formát, do kterého chcete exportovat. (V tomto výukovém kurzu se používá formát Microsoft Excel.)

![Datový projekt exportu pracovníků](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Zapamatujte si název projektu exportu dat. Budete ho potřebovat při vytváření logic app v dalším kroku.

### <a name="step-2-create-the-logic-app"></a>Krok 2: Vytvoření logic app

Sada cvičení zahrnuje vytvoření logic app.

1. Na portálu Azure vytvořte logic app.

    ![Stránka vytvoření logic app](media/integration-logic-app-creation-1.png)

2. V aplikaci Logic Apps Designer začněte s prázdnou logic app.
3. Přidejte [aktivační událost plánu opakování](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) pro spuštění logic app každých 24 hodin (nebo podle zvoleného plánu).

    ![Dialogové okno opakování](media/integration-logic-app-recurrence-step.png)

4. Volejte [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API pro naplánování exportu vašeho datového balíčku.

    1. Použijte akci **Vyvolat požadavek HTTP** z HTTP s konektorem Azure AD.

        - **Základní adresa URL zdroje** : adresa URL vašeho prostředí Human Resources (Nezahrnujte informace o cestě a oboru názvů.)
        - **URI zdroje Azure AD:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Služba Human Resources ještě neposkytuje konektor, který vystavuje všechna rozhraní API, která tvoří rozhraní REST API balíčku DMF, jako například **ExportToPackage**. Místo toho je nutné volat rozhraní API pomocí nezpracovaných požadavků HTTPS prostřednictvím protokolu HTTP s konektorem Azure AD. Tento konektor používá Azure Active Directory (Azure AD) pro ověřování a autorizaci Human Resources.

        ![HTTP s konektorem Azure AD](media/integration-logic-app-http-aad-connector-step.png)

    2. Přihlaste se ke svému prostředí Human Resources prostřednictvím protokolu HTTP s konektorem Azure AD.
    3. Nastavte požadavek HTTP **POST** na volání **ExportToPackage** DMF REST API.

        - **Metoda:** POST
        - **URL adresa požadavku:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Tělo požadavku:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Vyvolat akci požadavku HTTP](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Můžete chtít přejmenovat každý krok tak, aby byl výstižnější než výchozí název, **Vyvolat požadavek HTTP**. Tento krok můžete například přejmenovat na **ExportToPackage**.

5. [Inicializujte proměnnou](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) pro uložení stavu spuštění požadavku **ExportToPackage**.

    ![Akce inicializace proměnné](media/integration-logic-app-initialize-variable-step.png)

6. Počkejte, než bude stav spuštění exportu dat **Úspěšný**.

    1. Přidejte [do smyčky](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop), což se opakuje, než bude hodnota proměnné **ExecutionStatus** **Úspěšné**.
    2. Přidejte akci **zpoždění**, která počká pět sekund předtím, než se dotazuje na stav aktuálního spuštění exportu.

        ![Kontejner do smyčky](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Nastavte počet limitů na **15** a počkejte na dokončení exportu maximálně 75 sekund (15 iterací x 5 sekund). Pokud export trvá déle, upravte podle potřeby počet limitů.        

    3. Přidejte akci **Vyvolat požadavek HTTP** pro volání [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API a nastavte proměnnou **ExecutionStatus** na výsledek odpovědi **GetExecutionSummaryStatus**.

        > Tato ukázka neprovádí kontrolu chyb. Rozhraní API **GetExecutionSummaryStatus** může vracet neúspěšné stavy terminálu (ostatní stavy, než **úspěšné**). Další informace naleznete v [dokumentaci k rozhraní API](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Metoda:** POST
        - **URL adresa požadavku:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Tělo požadavku:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Je možné, že budete muset zadat hodnotu **Tělo požadavku** v zobrazení kódu nebo v editoru funkcí v návrháři.

        ![Vyvolat akci požadavku HTTP 2](media/integration-logic-app-get-execution-status-step.png)

        ![Nastavení akce proměnné](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > Hodnota akce **Nastavení proměnné** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) se bude lišit od hodnoty těla pro **Vyvolat požadavek HTTP 2**, a to i v případě, že návrhář zobrazí hodnoty stejným způsobem.

7. Získejte URL adresu stažení exportovaného balíčku.

    - Přidejte akci **Vyvolat požadavek HTTP** pro volání [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.

        - **Metoda:** POST
        - **URL adresa požadavku:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Tělo požadavku:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![Akce GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. Stáhněte exportovaný balíček.

    - Přidejte požadavek HTTP **GET** (vestavěnou [akci konektoru HTTP](https://docs.microsoft.com/azure/connectors/connectors-native-http)) a stáhněte balíček z URL adresy, která se vrátila v předchozím kroku.

        - **Metoda:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Je možné, že budete muset zadat hodnotu **URI** v zobrazení kódu nebo v editoru funkcí v návrháři.

        ![Akce HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Tento požadavek nevyžaduje žádné další ověření, protože adresa URL, kterou vrací **GetExportedPackageUrl** API, zahrnuje token podpisů sdílených přístupů, který uděluje přístup ke stažení souboru.

9. Uložte stažený balíček pomocí konektoru [OneDrive pro firmy](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness).

    - Přidejteakci [vytvoření souboru](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file)  OneDrive pro firmy.
    - Podle potřeby se připojte ke svému účtu OneDrive pro firmy.

        - **Cesta ke složce**: složka podle vašeho výběru
        - **Název souboru:** worker\_package.zip
        - **Obsah souboru:** tělo z předchozího kroku (dynamický obsah)

        ![Akce vytvoření souboru](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>Krok 3: Testování logic app

Chcete-li testovat logic app, vyberte v návrháři tlačítko **Spustit**. Uvidíte, že kroky spuštění logic app budou spuštěny. Po 30 až 40 sekundách by mělo být spuštění logic app dokončeno a složka OneDrive pro firmy by měla obsahovat nový soubor balíčku, který obsahuje exportované pracovníky.

Pokud je u některého kroku hlášeno selhání, vyberte v návrháři neúspěšný krok a zkontrolujte pole **Vstupy** a **Výstupy**. Proveďte ladění a upravte krok podle potřeby, aby se chyby opravily.

Následující obrázek ukazuje, jak vypadá aplikace Logic Apps Designer, když jsou všechny kroky logic app úspěšně spuštěny.

![Úspěšné spuštění logic app](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Souhrn

V tomto návodu jste se seznámili s použitím llogic app k exportu dat z Human Resources a k uložení exportovaných dat do složky OneDrive pro firmy. Kroky v tomto výukovém programu můžete upravit podle potřeb firmy.


