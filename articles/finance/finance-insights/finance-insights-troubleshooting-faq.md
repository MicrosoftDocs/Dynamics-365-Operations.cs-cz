---
title: Odstraňování problémů s nastavením Finance Insights
description: Toto téma uvádí seznam problémů, ke kterým může dojít při použití funkcí Finance Insights. Také vysvětluje, jak tyto problémy opravit.
author: panolte
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: fc616e5fce6bbfeaa3b36ccc35f1b1cf407af4a6
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109853"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Odstraňování problémů s nastavením Finance Insights

[!include [banner](../includes/banner.md)]

Toto téma uvádí seznam problémů, ke kterým může dojít při použití funkcí Finance Insights. Také vysvětluje, jak tyto problémy opravit.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Příznak: Proč nemohu namapovat cílový sloupec šablony Data Integration Přehledy plateb odběratele?

### <a name="resolution"></a>Řešení

Možná používáte šablonu pro dřívější verzi. Před vydáním verze 10.0.17 zákazníci preview konfigurovali šablonu Data Integration (DI) **Výsledky přehledu plateb odběratele (CDS do Fin and Ops)** pomocí entity **Výsledek předpovědi platby (preview)**. Po upgradu na verzi 10.0.17 a novější byste měli k dokončení mapování použít šablonu DI **Výsledky přehledu plateb odběratele (CDS na Fin a Ops 10.0.17 a novější)**. Je možné, že nebudete moci namapovat cílový sloupec šablony DI, dokud nebude aktualizován seznam entit správy dat a neobjeví se v něm entita **Výsledek předpovědi platby**. Chcete-li aktualizovat seznam entit a zobrazit výsledek předpovědi platby, dokončete kroky v obou portálech pro správu Microsoft Dynamics 365 Finance i Dataverse (dříve známé jako Common Data Service\[CDS\]).

### <a name="in-finance"></a>Ve Finance

Po upgradu postupujte ve Finance podle následujících kroků.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa dat**.
2. V pracovním prostoru **Správa dat** vyberte dlaždici **Parametry architektury**.
3. Na stránce **Parametry platformy importu a exportu dat** vyberte **Nastavení entity** a poté vyberte **Obnovit seznam entit**.
4. Zavřete stránku **Parametry platformy importu a exportu dat**.
5. V pracovním prostoru **Správa dat** vyberte dlaždici **Datové entity**.
6. Vyhledejte „Výsledek předpovědi platby“. Ověřte, že entita **Výsledek předpovědi platby** není ve verzi preview. Název verze preview končí řetězcem „(preview)“. Pokud vidíte pouze preview verzi entity, kontaktujte podporu Microsoftu.

### <a name="in-dataverse"></a>V Dataverse

Postupujte podle těchto kroků a v [centru pro správu Power Platform](https://admin.powerplatform.microsoft.com/environments) aktualizujte vaše projekty integrace dat.

1. Pokud používáte preview verzi Finance Insights, odeberte projekt DI, který je přidružen k šabloně **Výsledky přehledu plateb odběratele (CDS do Fin and Ops)**.
2. Postupujte podle pokynů v části [Vytvoření projektu integrátoru dat](create-data-integrate-project.md). Použijte šablonu **Výsledky přehledu plateb odběratele (CDS na Fin a Ops 10.0.17 a novější)**.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Příznak: Když se pokusím otevřít AI Builder pomocí odkazů na stránce nastavení Předpovědi plateb zákazníka, proč se mi zobrazuje následující chybová zpráva: „Je nám líto, ale došlo k odpojení“?

### <a name="resolution"></a>Řešení

Uživatelé Dynamics 365 Finance musí mít uživatelský účet Microsoft Power Apps pro dané prostředí a tento uživatelský účet musí mít roli přizpůsobení systému. Správce systému Microsoft Power Apps může vytvořit uživatelský účet a přiřadit roli. Poté můžete přejít na <https://make.preview.powerapps.com/>, přihlásit se pomocí tohoto uživatelského účtu a zkusit odkazy znovu.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Příznak: Proč karta Předpověď hotovosti v pracovním prostoru Prognóza cashflow nezobrazuje žádná data?

### <a name="resolution"></a>Řešení

Aby bylo možné správně zobrazovat data v pracovním prostoru **Prognóza cashflow**, musí být nastavena a povolena funkce prognózy cashflow ve správě pokladny a banky a funkce prognózy cashflow ve Finance Insights.

Nejprve nastavte a povolte prognózu cashflow a účty likvidity. Více informací získáte v části [Prognóza cashflow](../cash-bank-management/cash-flow-forecasting.md). Pokud bylo toto nastavení dokončeno, ale nevidíte očekávané výsledky, pročtěte si další informace v tématu [Řešení potíží s nastavením předpovědi cashflow](../cash-bank-management/cash-flow-forecasting-tsg.md).

Dále potvrďte, že funkce prognózy cashflow ve Finance Insights (**Správa pokladny a banky \> Nastavení \> Finance Insights \> Prognózy cashflow**) byla povolena a trénování modelu AI bylo dokončeno. Pokud trénování nebylo dokončeno, vyberte **Prognóza teď** a zahajte proces trénování modelu.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Příznak: Proč není tlačítko Instalovat nový doplněk vidět v Microsoft Dynamics Lifecycle Services?

### <a name="resolution"></a>Řešení

Nejprve ověřte, že jsou role **Manažer prostředí** nebo **Vlastník projektu** přiřazeny přihlášenéu uživateli v poli **Role zabezpečení projektu** v Microsoft Dynamics Lifecycle Services (LCS). Instalace nových doplňků vyžaduje jednu z těchto rolí zabezpečení projektu.

Pokud je vám přiřazena správná role zabezpečení projektu, možná budete muset obnovit okno prohlížeče, abyste viděli tlačítko **Nainstalovat nový doplněk**.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Příznak: Zdá se, že doplněk Finance insights se neinstaluje. Proč?

### <a name="resolution"></a>Řešení

Následující kroky by měly být dokončeny.

- Ověřte, že máte přístup **Správce systému** a **Kustomizer systému** v centru pro správu Power Portal.
- Ověřte, že je použita licence Dynamics 365 Finance nebo ekvivalentní licence na uživatele, který instaluje doplněk.
- Ověřte, že následující aplikace Azure AD je registrována v Azure AD: 

  | Přihláška                  | ID aplikace           |
  | ---------------------------- | ---------------- |
  | Mikroslužby CDS Microsoft Dynamics ERP | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Příznak: Chyba: „Nenalezli jsme žádná data pro vybraný rozsah filtru. Vyberte jiný rozsah filtru a zkuste to znovu.“ 

### <a name="resolution"></a>Řešení

Zkontrolujte nastavení integrátoru dat, abyste ověřili, že funguje podle očekávání, a odesílá data z AI Builder zpět do Finance.  
Další informace naleznete v tématu [Vytvoření projektu integrace dat](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Příznak: Trénování předpovědi plateb zákazníka se nezdařilo a chyba AI Builder uvádí : „Předpověď musí mít pouze dvě různé výsledné hodnoty pro trénování modelu. Mapujte na dva výsledky a znovu natrénujte“, „Problém se zprávou o trénování: IsNotMinRequiredDistinctNonNullValues“.

### <a name="resolution"></a>Řešení

Tato chyba znamená, že v posledním roce není dostatek historických transakcí, které představují každou kategorii popsanou v kategoriích **Včas**, **Pozdě** a **Velmi pozdě**. Chcete-li tuto chybu vyřešit, upravte období transakce **Velmi pozdě**. Pokud úprava období transakce **Velmi pozdě** chybu neopraví, **Předpovědi plateb zákazníků** není nejlepším řešením, protože potřebuje data v každé kategorii pro účely trénování.

Další informace o tom, jak upravit kategorie **Včas**, **Pozdě** a **Velmi pozdě** viz [Aktivace předpovědí plateb zákazníků](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Příznak: Trénink modelu selhal

### <a name="resolution"></a>Řešení

Trénink modelu **Předpověď peněžních toků** vyžaduje data se 100 nebo více transakcemi, která pokrývají více než jeden rok. Doporučujeme mít alespoň dva roky dat s více než 1 000 transakcemi.

Funkce **Předpovědi plateb zákazníků** vyžaduje více než 100 transakcí za předchozích šest až devět měsíců. Transakce mohou zahrnovat volné faktury, prodejní objednávky a platby zákazníků. Tato data musí být rozložena do všech nastavení **Včas**, **Pozdě** a **Velmi pozdě**, která jsou definována na stránce **Konfigurace**.    

Funkce **Návrh rozpočtu** vyžaduje minimálně tři roky rozpočtových nebo skutečných údajů. Toto řešení používá v projekcích data za tři až deset let. Data za více než tři roky poskytují lepší výsledky. Data samotná fungují nejlépe, když se hodnoty liší. Pokud data obsahují pouze konstantní data, jako jsou náklady na pronájem, může trénink selhat, protože nedostatek variací nevyžaduje, aby AI promítla částky.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>Příznak: Chybová zpráva uvádí, že "Tabulka s názvem, 'msdyn_paypredpredictionresultentities' neexistuje. Vzdálený server vrátil chybu: (404) Nenalezeno…"

### <a name="resolution"></a>Řešení

Prostředí dosáhlo maximálního limitu tabulky služeb Data Lake. Další informace o limitu naleznete v oddílu **Povolit změny dat téměř v reálném čase** tématu [Přehled exportu do Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md).
