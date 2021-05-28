---
title: Zaznamenání čísel koncesních certifikátů TDS
description: Toto téma vysvětluje, jak zaznamenat čísla koncesních certifikátů daně odečtené u zdroje (TDS), která jsou vydávána prodejcům.
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023076"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="c98e4-103">Zaznamenání čísel koncesních certifikátů TDS</span><span class="sxs-lookup"><span data-stu-id="c98e4-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c98e4-104">Toto téma vysvětluje, jak zaznamenat čísla koncesních certifikátů daně odečtené u zdroje (TDS), která jsou vydávána prodejcům.</span><span class="sxs-lookup"><span data-stu-id="c98e4-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="c98e4-105">Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Koncese srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="c98e4-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="c98e4-106">V poli **Typ daně** vyberte **TDS** k zaznamenání koncesních certifikátů pro daňový typ TDS.</span><span class="sxs-lookup"><span data-stu-id="c98e4-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="c98e4-107">Na kartě **Přehled** vyberte **Alt + N** k vytvoření řádku.</span><span class="sxs-lookup"><span data-stu-id="c98e4-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="c98e4-108">[![Záhlaví nového řádku](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="c98e4-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="c98e4-109">V poli **Kód srážkové daně** vyberte daňový kód TDS, pro který jsou vydány koncesní certifikáty dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c98e4-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="c98e4-110">Pole **Název srážkové daně** zobrazuje název kódu daně TDS.</span><span class="sxs-lookup"><span data-stu-id="c98e4-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="c98e4-111">V polích **Od data** a **Do data** definujte dobu platnosti koncesního certifikátu, který používá daňový kód TDS k výpočtu TDS koncesně.</span><span class="sxs-lookup"><span data-stu-id="c98e4-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="c98e4-112">Do pole **Poznámky** zadejte jakékoli poznámky.</span><span class="sxs-lookup"><span data-stu-id="c98e4-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="c98e4-113">V poli **Oddíl** zadejte kód oddílu zákona, pod kterým je koncesní certifikát TDS vydáván.</span><span class="sxs-lookup"><span data-stu-id="c98e4-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="c98e4-114">Pokud je kód oddílu 197, hodnota „A“ se objeví ve sloupci „Důvod pro neodpočítávání / nižší odpočet“ ve formuláři 26Q a ve sloupci „Důvod pro neodpočítávání / nižší odpočet / přepočítání (pokud existuje)“ ve formulářu 27Q.</span><span class="sxs-lookup"><span data-stu-id="c98e4-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="c98e4-115">Pokud je kód sekce 197A, zobrazí se na obou těchto místech hodnota „B“.</span><span class="sxs-lookup"><span data-stu-id="c98e4-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="c98e4-116">Vyberte pevnou kartu **Certifikát** pro záznam čísel koncesních certifikátů TDS pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c98e4-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="c98e4-117">V poli **Účet dodavatele** vyberte účet dodavatele, pro který je vydán koncesní certifikát TDS.</span><span class="sxs-lookup"><span data-stu-id="c98e4-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="c98e4-118">V polích **Od data** a **K datu** definujte dobu platnosti koncesního certifikátu TDS.</span><span class="sxs-lookup"><span data-stu-id="c98e4-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="c98e4-119">Výpočet TDS na základě zvýhodnění je založen na období, kdy je certifikát pro dodavatele vytvořen.</span><span class="sxs-lookup"><span data-stu-id="c98e4-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="c98e4-120">Do pole **Certifikát** zadejte číslo koncesního certifikátu TDS.</span><span class="sxs-lookup"><span data-stu-id="c98e4-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="c98e4-121">[![Pevná záložka Certifikát](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="c98e4-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="c98e4-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c98e4-122">Close the page.</span></span>
