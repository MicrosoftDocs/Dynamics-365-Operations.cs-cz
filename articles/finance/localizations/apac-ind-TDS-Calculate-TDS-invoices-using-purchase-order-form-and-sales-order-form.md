---
title: Výpočet faktur TDS pomocí formuláře nákupní objednávky a formuláře prodejní objednávky
description: Toto téma obsahuje kroky pro výpočet daně odečtené u zdroje (TDS) u různých typů faktur.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023078"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="98f6a-103">Výpočet faktur TDS pomocí formuláře nákupní objednávky a formuláře prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="98f6a-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98f6a-104">Toto téma obsahuje kroky pro výpočet daně odečtené u zdroje (TDS) u různých typů faktur pomocí stránek **Nákupní objednávka**, **Deník nákupů**, **Paušální objednávka** a **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="98f6a-105">Pomocí uvedené stránky vytvoříte nákupní objednávku, deník nákupu, paušální nákupní objednávku nebo prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="98f6a-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="98f6a-106">Zadejte požadované údaje.</span><span class="sxs-lookup"><span data-stu-id="98f6a-106">Enter the required details.</span></span>

2. <span data-ttu-id="98f6a-107">Vyberte kartu **Nastavení** pro zobrazení povahy hodnotitele dodavatele nebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="98f6a-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="98f6a-108">Tyto informace jsou uvedeny v poli **Povaha posuzovaného** pod skupinou poli **Skupina pro srážkovou daň**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="98f6a-109">V poli **Skupina TDS** zobrazte nebo upravte výchozí skupinu TDS definovanou pro dodavatele nebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="98f6a-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="98f6a-110">Pole **Skupina TCS** není k dispozici, když vyberete skupinu TDS v poli **Skupina TDS**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="98f6a-111">TDS se počítá, pouze pokud je zaškrtnuté políčko **Vypočítat srážkovou daň** pro dodavatele nebo zákazníka na stránce **Všichni dodavatelé** nebo **Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="98f6a-112">Vytvořte řádky položek na kartě **Řádky** a zadejte požadované údaje.</span><span class="sxs-lookup"><span data-stu-id="98f6a-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="98f6a-113">Vyberte kartu **Nastavení** (na úrovni řádku) pro zobrazení nebo změnu skupiny TDS definované na úrovni záhlaví.</span><span class="sxs-lookup"><span data-stu-id="98f6a-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="98f6a-114">Skupina TDS je zobrazena v poli **Skupina TDS**, které je pod skupinou polí **Skupina pro srážkovou daň**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="98f6a-115">Vyberte kartu **Daňové údaje** a vyberte alternativní adresy, které jsou nastaveny pro název společnosti, který se zobrazuje v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="98f6a-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="98f6a-116">Název společnosti je zobrazen v poli **Název**, které je pod skupinou polí **Údaje o společnosti**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="98f6a-117">TAN vybraného názvu společnosti se zobrazí v poli **Číslo daňového účtu** (**TAN**) pod skupinou polí **Srážková daň**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="98f6a-118">Vyberte **Srážková daň** k otevření stránky **Dočasné transakce srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="98f6a-119">Zobrazte následující pole v horním podokně stránky **Dočasné transakce srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="98f6a-120">**Částka** **srážkové** **daně** **celkem** – Celková TDS, která byla vypočítána pro transakci pro skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="98f6a-121">**Hodnota** – Celkové procento, které bylo použito k výpočtu TDS pro transakci.</span><span class="sxs-lookup"><span data-stu-id="98f6a-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="98f6a-122">Celkové procento je založeno na vzorci, který je definován pro daňové kódy TDS a je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="98f6a-123">**Upravená částka srážkové daně celkem** – Celková upravená částka TDS pro všechny daňové kódy ve skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="98f6a-124">**TDS** – Pokud je vybráno, je k transakci připojena skupina TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="98f6a-125">Políčka na kartách **Přehled**, **Všeobecné** a **Vyrovnání** na stránce **Dočasné transakce srážkové daně** zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="98f6a-126">Vybrat **Mezní hodnota** k otevření stránky **Mezní hodnota**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="98f6a-127">Na této stránce si můžete prohlédnout mezní hodnotu definovanou pro daňovou složku TDS připojenou ke konkrétnímu daňovému kódu TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="98f6a-128">Vyberte **Návrhář vzorců** k otevření stránky **Návrhář vzorců**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="98f6a-129">Na této stránce si můžete prohlédnout vzorec definovaný pro konkrétní daňový kód TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="98f6a-130">Zaúčtujte fakturu.</span><span class="sxs-lookup"><span data-stu-id="98f6a-130">Post the invoice.</span></span> <span data-ttu-id="98f6a-131">Částka TDS vypočtená z nákupních faktur se zaúčtuje na účet závazků a částka TDS vypočítaná z prodejních faktur se zaúčtuje na účet pohledávek, který je definován pro každý daňový kód TDS ve skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="98f6a-132">Účty závazků nebo účty pohledávek pro daňové kódy TDS jsou definovány na stránce **Kódy srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="98f6a-133">Vyberte tlačítko **Dotaz** **> Faktura > Zaúčtovaná srážková daň** k otevření stránky **Transakce srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="98f6a-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="98f6a-134">Pole **Hodnota** zobrazuje celkové procento, které bylo použito k výpočtu TDS pro transakci.</span><span class="sxs-lookup"><span data-stu-id="98f6a-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="98f6a-135">Pole na kartách **Přehled**, **Všeobecné** a **Částka** na stránce **Transakce srážkové daně** zobrazuje informace TDS vypočítané pro transakci.</span><span class="sxs-lookup"><span data-stu-id="98f6a-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="98f6a-136">Zkontrolujte informace o výpočtu TDS pro každý daňový kód TDS, který je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="98f6a-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
