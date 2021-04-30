---
title: Použití externích dat v prognózách peněžních toků (náhled)
description: Toto téma popisuje kroky nastavení, které musíte provést, aby bylo možné do prognóz peněžních toků zadávat nebo importovat externí data.
author: rcarlson
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ddfc0670a5fca24d996e9ab605e267f9f3f26f19
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897881"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="a3e53-103">Použití externích dat v prognózách peněžních toků (náhled)</span><span class="sxs-lookup"><span data-stu-id="a3e53-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a3e53-104">Externí data lze zadávat nebo importovat do prognóz peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="a3e53-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="a3e53-105">Toto téma popisuje kroky nastavení, které jsou specifické pro použití externích dat a které umožňují zahrnutí externích dat do prognózy peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="a3e53-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="a3e53-106">Nastavení externích dat</span><span class="sxs-lookup"><span data-stu-id="a3e53-106">External data setup</span></span>

<span data-ttu-id="a3e53-107">Použijte kartu **Vnější zdroj** na stránce **Nastavení předpovědi peněžních toků** (**Pokladna a banka \> Prognóza peněžních toků**) a zadejte nastavení, která podporují použití externích dat v předpovědích peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="a3e53-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="a3e53-108">Další informace o nastavení čítačů naleznete v tématu [Prognóza cashflow](../cash-bank-management/cash-flow-forecasting.md).</span><span class="sxs-lookup"><span data-stu-id="a3e53-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="a3e53-109">Chcete-li zadat externí data pro prognózy peněžních toků, můžete k zadávání a úpravě externích dat použít prostředí Otevřít v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="a3e53-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="a3e53-110">Vyberte tlačítko **Externí data** a poté vyberte **Přidat externí data** nebo **Upravit existující externí data**.</span><span class="sxs-lookup"><span data-stu-id="a3e53-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="a3e53-111">Když je soubor Microsoft Excel otevřen, můžete zadat informace do následujících polí:</span><span class="sxs-lookup"><span data-stu-id="a3e53-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="a3e53-112">**ID položky**</span><span class="sxs-lookup"><span data-stu-id="a3e53-112">**Entry ID**</span></span>
- <span data-ttu-id="a3e53-113">**Popis** (nepovinné)</span><span class="sxs-lookup"><span data-stu-id="a3e53-113">**Description** (optional)</span></span>
- <span data-ttu-id="a3e53-114">**Název externího zdroje** - Vyberte jednu z hodnot v seznamu, který jste definovali při nastavování nástroje Finanční přehledy.</span><span class="sxs-lookup"><span data-stu-id="a3e53-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="a3e53-115">**Právnická osoba**</span><span class="sxs-lookup"><span data-stu-id="a3e53-115">**Legal Entity**</span></span>
- <span data-ttu-id="a3e53-116">**Datum**</span><span class="sxs-lookup"><span data-stu-id="a3e53-116">**Date**</span></span>
- <span data-ttu-id="a3e53-117">**Částka v měně transakce**</span><span class="sxs-lookup"><span data-stu-id="a3e53-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="a3e53-118">**Kód měny**</span><span class="sxs-lookup"><span data-stu-id="a3e53-118">**Currency Code**</span></span>
- <span data-ttu-id="a3e53-119">**Výchozí dimenze** (volitelný)</span><span class="sxs-lookup"><span data-stu-id="a3e53-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="a3e53-120">**Číslo dokumentu** (volitelný)</span><span class="sxs-lookup"><span data-stu-id="a3e53-120">**Document number** (optional)</span></span>
- <span data-ttu-id="a3e53-121">**Číslo účtu** (volitelný)</span><span class="sxs-lookup"><span data-stu-id="a3e53-121">**Account number** (optional)</span></span>
- <span data-ttu-id="a3e53-122">**Název účtu** (volitelný)</span><span class="sxs-lookup"><span data-stu-id="a3e53-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="a3e53-123">Import externích dat pomocí rámce Správy dat</span><span class="sxs-lookup"><span data-stu-id="a3e53-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="a3e53-124">Můžete importovat externí data pro předpovědi peněžních toků pomocí pracovního prostoru **Správa dat** a entity, která se jmenuje **Předpověď peněžního toku externího vstupu zdroje**.</span><span class="sxs-lookup"><span data-stu-id="a3e53-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="a3e53-125">Kromě toho, pokud musíte přesunout data nastavení z jednoho prostředí do jiného, je pro tyto tabulky nastavení k dispozici následující oblast entit:</span><span class="sxs-lookup"><span data-stu-id="a3e53-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="a3e53-126">Nastavení externího zdroje prognózy cashflow</span><span class="sxs-lookup"><span data-stu-id="a3e53-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="a3e53-127">Nastavení právnické osoby externího zdroje prognózy cashflow</span><span class="sxs-lookup"><span data-stu-id="a3e53-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="a3e53-128">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="a3e53-128">Privacy notice</span></span>
<span data-ttu-id="a3e53-129">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="a3e53-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]