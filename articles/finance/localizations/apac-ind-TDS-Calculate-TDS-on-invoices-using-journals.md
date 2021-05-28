---
title: Výpočet TDS na fakturách pomocí deníků
description: Toto téma obsahuje kroky pro výpočet daně odečtené u zdroje (TDS) u deníků.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023102"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="4fc5c-103">Výpočet TDS na fakturách pomocí deníků</span><span class="sxs-lookup"><span data-stu-id="4fc5c-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fc5c-104">Toto téma obsahuje kroky pro výpočet daně odečtené u zdroje (TDS) u deníků.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="4fc5c-105">Začněte otevřením stránky **Hlavní knihy** (**Hlavní kniha > Položky deníku > Hlavní deníky**).</span><span class="sxs-lookup"><span data-stu-id="4fc5c-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="4fc5c-106">[![Hlavní deníky](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="4fc5c-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="4fc5c-107">Vytvořte řádky deníku pomocí formulářů deníku, které jsou uvedeny v tabulce.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="4fc5c-108">Vyberte typ účtu a typ protiúčtu a zadejte částku za transakci.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="4fc5c-109">Na stránce **Deník schválení faktury** vyberte **Najít doklady** a vyberte faktury pro výpočet TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="4fc5c-110">Zobrazte faktury vytvořené na stránce **Registr faktur** nebo stránce **Najít doklady**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="4fc5c-111">Na kartě **Obecné** stránky **Doklad deníku** v poli **Skupiny TDS** zkontrolujte nebo změňte výchozí skupinu TDS definovanou pro dodavatele nebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="4fc5c-112">Částka TDS, která se počítá na řádcích deníku, je založena na vzorci, který je definován pro daňové kódy TDS ve **skupině TDS**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="4fc5c-113">Když v seznamu vyberete skupinu TDS v poli **Skupina TDS**, pole **Skupina pro srážkovou daň** a **Skupina TCS** nebudou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="4fc5c-114">Pole **Skupina pro srážkovou daň** je k dispozici pouze na stránce **Obecný deník**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="4fc5c-115">TDS se počítá, pouze pokud je zaškrtnuté políčko **Vypočítat srážkovou daň** pro dodavatele nebo zákazníka na stránce **Všichni dodavatelé** nebo **Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="4fc5c-116">Vyberte kartu **Daňové údaje**. V případě potřeby vyberte alternativní adresy společnosti, které jsou nastaveny pro společnost v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="4fc5c-117">Název společnosti je zobrazen v poli **Název**, které je pod skupinou polí **Údaje o společnosti**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="4fc5c-118">Ve skupině polí **Srážková daň** v poli **Povaha posuzovaného** naleznete povahu hodnocené kategorie dodavatele nebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="4fc5c-119">V poli **Číslo daňového účtu** (**TAN**) vidíte TAN vybraného názvu společnosti, který se zobrazí.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="4fc5c-120">Vyberte **Srážková daň** v nabídce **Srážková daň** k otevřené stránky **Dočasné transakce srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="4fc5c-121">V horním podokně stránky **Dočasné transakce srážkové daně** se zobrazí následující pole.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="4fc5c-122">**Částka srážkové daně celkem** – Celková TDS, která byla vypočítána pro transakci pro skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="4fc5c-123">**Hodnota** – Celkové procento, které bylo použito k výpočtu TDS pro transakci.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="4fc5c-124">Celkové procento je založeno na vzorci, který je definován pro daňové kódy TDS a je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="4fc5c-125">**Upravená částka srážkové daně celkem** – Celková upravená částka TDS pro všechny daňové kódy ve skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="4fc5c-126">**TDS** – Pokud je vybráno, je k transakci připojena skupina TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="4fc5c-127">Políčka na kartách **Přehled**, **Všeobecné** a **Vyrovnání** na stránce **Dočasné transakce srážkové daně** zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="4fc5c-128">Vybrat **Mezní hodnota** k otevření stránky **Mezní hodnota**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="4fc5c-129">Na této stránce si můžete prohlédnout mezní hodnotu a mezní hodnotu výjimky definovanou pro daňovou složku TDS připojenou ke konkrétnímu daňovému kódu TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="4fc5c-130">Vyberte **Návrhář vzorců** k otevření formuláře **Návrhář vzorců**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="4fc5c-131">Na této stránce si můžete prohlédnout vzorec definovaný pro konkrétní daňový kód TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="4fc5c-132">Zavřete stránky **Návrhář vzorců** a **Dočasné transakce srážkové daně** pro návrat na stránku **Doklad deníku** .</span><span class="sxs-lookup"><span data-stu-id="4fc5c-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="4fc5c-133">Zadejte další požadované údaje.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-133">Enter the other required details.</span></span> <span data-ttu-id="4fc5c-134">Proveďte ověření a zaúčtování deníku.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-134">Validate and post the journal.</span></span> <span data-ttu-id="4fc5c-135">Částka TDS, která se počítá z nákupních faktur, se zaúčtuje na účet závazků.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="4fc5c-136">Vypočítaná částka TDS, která je vypočítána na prodejních fakturách, se zaúčtuje na účet pohledávek, který je definován pro každý daňový zákon TDS ve skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="4fc5c-137">Účty závazků nebo účty pohledávek pro daňové kódy TDS jsou definovány na stránce **Kódy srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="4fc5c-138">Vyberte **Zaúčtovaná srážková daň** k otevření stránky **Transakce** **srážkové** **daně**.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="4fc5c-139">Pole **Hodnota** zobrazuje celkové procento, které bylo použito k výpočtu TDS pro transakci.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="4fc5c-140">Políčka na kartách **Přehled**, **Všeobecné** a **Částka** na stránce Dočasné transakce srážkové daně zobrazují vypočítanou částku TDS a údaje o upravené částce TDS pro každý daňový zákon TDS, který je připojen ke skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="4fc5c-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
