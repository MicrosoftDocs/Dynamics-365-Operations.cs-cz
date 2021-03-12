---
title: Změna způsobu dodání v POS
description: Toto téma popisuje, jak konfigurovat a používat operaci změny způsobu dodání v POS.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6bfe27a7b4a768da00c67e307a0bd7e57b333d11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965420"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="ee009-103">Změna způsobu dodání v POS</span><span class="sxs-lookup"><span data-stu-id="ee009-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ee009-104">Tohle téma popisuje, jak nastavit a používat funkci „Změnit způsob dodání“ v prostředí pokladního místa (POS).</span><span class="sxs-lookup"><span data-stu-id="ee009-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="ee009-105">V Dynamics 365 Commerce verze 10.0.10 a novějších je k dispozici operace **Změnit způsob dodání** (647), která slouží pro přidání vašich rozložení obrazovky POS.</span><span class="sxs-lookup"><span data-stu-id="ee009-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="ee009-106">Funkce změny způsobu dodání umožňuje změnit způsob dodání pro jeden nebo více prodejních řádků konfigurovaných pro dodávku v transakci POS.</span><span class="sxs-lookup"><span data-stu-id="ee009-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="ee009-107">V předchozích verzích Commerce bylo nutné projít celé toky konfigurace **Odeslat vše** nebo **Odeslat vybrané**, pokud jste chtěli změnit způsob dodání na existujícím řádku nakonfigurovaném pro expedici.</span><span class="sxs-lookup"><span data-stu-id="ee009-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="ee009-108">Tento proces byl časově náročný a mohl vést k neúmyslným změnám původu dodávky nebo dat dodání pro daný řádek.</span><span class="sxs-lookup"><span data-stu-id="ee009-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="ee009-109">Nová funkce poskytuje alternativní metodu pro efektivní aktualizaci způsobu dodání na těchto řádcích prodeje.</span><span class="sxs-lookup"><span data-stu-id="ee009-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="ee009-110">Další informace, jak přidat operaci k tlačítku v mřížce tlačítek POS, viz [Rozložení obrazovky pokladního místa](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="ee009-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="ee009-111">Po konfiguraci této funkce v aplikaci POS se při výběru možnosti **Změnit způsob dodání** zobrazí stránka se seznamem, která vám umožní vybrat řádky transakce, pro které chcete změnit způsob dodání.</span><span class="sxs-lookup"><span data-stu-id="ee009-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="ee009-112">Můžete vybrat některé nebo všechny řádky nebo ukončit aplikaci bez provedení změn.</span><span class="sxs-lookup"><span data-stu-id="ee009-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="ee009-113">Řádky prodeje, které byly dříve konfigurovány pro dodávku, jsou jediné řádky v seznamu, které lze změnit.</span><span class="sxs-lookup"><span data-stu-id="ee009-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="ee009-114">Chcete-li změnit řádek určený k výdeji nebo převzetí a předání k expedici, je nutné použít operace **Odeslat vše** nebo **Odeslat vybrané**.</span><span class="sxs-lookup"><span data-stu-id="ee009-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="ee009-115">Chcete-li naopak změnit řádek určený jako dodávka k vyzvednutí nebo převzetí, musíte použít operace **Vyzvednout vše**, **Vyzvednout vybrané**, **Převzít vše** nebo **Převzít vybrané**.</span><span class="sxs-lookup"><span data-stu-id="ee009-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="ee009-116">Po vybrání řádků, které chcete změnit, klikněte na možnost **Změnit způsob dodání**, abyste mohli vybrat možnosti způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="ee009-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="ee009-117">Pokud jste vybrali více řádků, které chcete změnit, zobrazí se v POS pouze způsoby dodání, které byly pro všechny vybrané produkty nakonfigurovány jako povolené.</span><span class="sxs-lookup"><span data-stu-id="ee009-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="ee009-118">Způsoby dodání lze nakonfigurovat tak, aby podporovaly specifické produkty a dodací adresy.</span><span class="sxs-lookup"><span data-stu-id="ee009-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="ee009-119">Pokud existuje způsob dodání, který je přijatelný pro jednu kombinaci produktů a adres, ale není přijatelný pro jinou kombinaci vybraného produktu a adresy, není režim dodání k dispozici.</span><span class="sxs-lookup"><span data-stu-id="ee009-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="ee009-120">Je možné, že budete muset vybrat řádky jeden po druhém a změnit způsob dodání pro každý řádek zvlášť, pokud chcete vybrat způsob dodání pro jeden produkt, který není podporován jiným produktem.</span><span class="sxs-lookup"><span data-stu-id="ee009-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="ee009-121">Po výběru nového způsobu dodání se zobrazí stránka transakce.</span><span class="sxs-lookup"><span data-stu-id="ee009-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="ee009-122">Chcete-li zkontrolovat nové výběry způsobu dodání, vyberte kartu **Doručení** v seznamu transakcí.</span><span class="sxs-lookup"><span data-stu-id="ee009-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee009-123">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ee009-123">Additional resources</span></span>

[<span data-ttu-id="ee009-124">Vytváření objednávek v kontaktním středisku</span><span class="sxs-lookup"><span data-stu-id="ee009-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="ee009-125">Přizpůsobení transakčních e-mailů podle způsobu doručení</span><span class="sxs-lookup"><span data-stu-id="ee009-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)
