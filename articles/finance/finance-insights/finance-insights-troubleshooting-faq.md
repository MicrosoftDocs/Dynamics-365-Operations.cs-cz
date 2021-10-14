---
title: Odstraňování problémů s nastavením Finance Insights
description: Toto téma uvádí seznam problémů, ke kterým může dojít při použití funkcí Finance Insights. Také vysvětluje, jak tyto problémy opravit.
author: panolte
ms.date: 08/20/2021
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
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512883"
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

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Příznak: Proč karta Předpověď hotovosti v pracovním prostoru Prognóza cashflow nezobrazuje žádná data?

### <a name="resolution"></a>Řešení

Aby bylo možné správně zobrazovat data v pracovním prostoru **Prognóza cashflow**, musí být nastavena a povolena funkce prognózy cashflow ve správě pokladny a banky a funkce prognózy cashflow ve Finance Insights.

Nejprve nastavte a povolte prognózu cashflow a účty likvidity. Více informací získáte v části [Prognóza cashflow](../cash-bank-management/cash-flow-forecasting.md). Pokud bylo toto nastavení dokončeno, ale nevidíte očekávané výsledky, pročtěte si další informace v tématu [Řešení potíží s nastavením předpovědi cashflow](../cash-bank-management/cash-flow-forecasting-tsg.md).

Dále potvrďte, že funkce prognózy cashflow ve Finance Insights (**Správa pokladny a banky \> Nastavení \> Finance Insights \> Prognózy cashflow**) byla povolena a trénování modelu AI bylo dokončeno. Pokud trénování nebylo dokončeno, vyberte **Prognóza teď** a zahajte proces trénování modelu.
