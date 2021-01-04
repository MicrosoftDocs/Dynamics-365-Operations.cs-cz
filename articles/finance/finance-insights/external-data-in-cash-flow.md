---
title: Použití externích dat v prognózách peněžních toků (náhled)
description: Toto téma popisuje kroky nastavení, které musíte provést, aby bylo možné do prognóz peněžních toků zadávat nebo importovat externí data.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 801327dc54f6d4cfef7a9f062395e29846783e8f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644938"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="00d9a-103">Použití externích dat v prognózách peněžních toků (náhled)</span><span class="sxs-lookup"><span data-stu-id="00d9a-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="00d9a-104">Externí data lze zadávat nebo importovat do prognóz peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="00d9a-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="00d9a-105">Toto téma popisuje kroky nastavení, které jsou specifické pro použití externích dat a které umožňují zahrnutí externích dat do prognózy peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="00d9a-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="00d9a-106">Nastavení externích dat</span><span class="sxs-lookup"><span data-stu-id="00d9a-106">External data setup</span></span>

<span data-ttu-id="00d9a-107">Použijte kartu **Vnější zdroj** na stránce **Nastavení předpovědi peněžních toků** (**Pokladna a banka \> Prognóza peněžních toků**) a zadejte nastavení, která podporují použití externích dat v předpovědích peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="00d9a-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="00d9a-108">Další informace o nastavení čítačů naleznete v tématu [Prognóza cashflow](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="00d9a-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="00d9a-109">Chcete-li zadat externí data pro prognózy peněžních toků, můžete k zadávání a úpravě externích dat použít prostředí Otevřít v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="00d9a-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="00d9a-110">Vyberte tlačítko **Externí data** a poté vyberte **Přidat externí data** nebo **Upravit existující externí data**.</span><span class="sxs-lookup"><span data-stu-id="00d9a-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="00d9a-111">Když je soubor Microsoft Excel otevřen, můžete zadat informace do následujících polí:</span><span class="sxs-lookup"><span data-stu-id="00d9a-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="00d9a-112">**ID položky**</span><span class="sxs-lookup"><span data-stu-id="00d9a-112">**Entry ID**</span></span>
- <span data-ttu-id="00d9a-113">**Popis** (nepovinné)</span><span class="sxs-lookup"><span data-stu-id="00d9a-113">**Description** (optional)</span></span>
- <span data-ttu-id="00d9a-114">**Název externího zdroje** - Vyberte jednu z hodnot v seznamu, který jste definovali při nastavování nástroje Finanční přehledy.</span><span class="sxs-lookup"><span data-stu-id="00d9a-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="00d9a-115">**Právnická osoba**</span><span class="sxs-lookup"><span data-stu-id="00d9a-115">**Legal Entity**</span></span>
- <span data-ttu-id="00d9a-116">**Datum**</span><span class="sxs-lookup"><span data-stu-id="00d9a-116">**Date**</span></span>
- <span data-ttu-id="00d9a-117">**Částka v měně transakce**</span><span class="sxs-lookup"><span data-stu-id="00d9a-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="00d9a-118">**Kód měny**</span><span class="sxs-lookup"><span data-stu-id="00d9a-118">**Currency Code**</span></span>
- <span data-ttu-id="00d9a-119">**Výchozí dimenze** (volitelný)</span><span class="sxs-lookup"><span data-stu-id="00d9a-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="00d9a-120">**Číslo dokumentu** (volitelný)</span><span class="sxs-lookup"><span data-stu-id="00d9a-120">**Document number** (optional)</span></span>
- <span data-ttu-id="00d9a-121">**Číslo účtu** (volitelný)</span><span class="sxs-lookup"><span data-stu-id="00d9a-121">**Account number** (optional)</span></span>
- <span data-ttu-id="00d9a-122">**Název účtu** (volitelný)</span><span class="sxs-lookup"><span data-stu-id="00d9a-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="00d9a-123">Import externích dat pomocí rámce Správy dat</span><span class="sxs-lookup"><span data-stu-id="00d9a-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="00d9a-124">Můžete importovat externí data pro předpovědi peněžních toků pomocí pracovního prostoru **Správa dat** a entity, která se jmenuje **Předpověď peněžního toku externího vstupu zdroje**.</span><span class="sxs-lookup"><span data-stu-id="00d9a-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="00d9a-125">Kromě toho, pokud musíte přesunout data nastavení z jednoho prostředí do jiného, je pro tyto tabulky nastavení k dispozici následující oblast entit:</span><span class="sxs-lookup"><span data-stu-id="00d9a-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="00d9a-126">Nastavení externího zdroje prognózy cashflow</span><span class="sxs-lookup"><span data-stu-id="00d9a-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="00d9a-127">Nastavení právnické osoby externího zdroje prognózy cashflow</span><span class="sxs-lookup"><span data-stu-id="00d9a-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="00d9a-128">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="00d9a-128">Privacy notice</span></span>
<span data-ttu-id="00d9a-129">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="00d9a-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
