---
title: Nastavení indexových sazeb
description: Toto téma vysvětluje, jak nastavit indexové sazby. Indexové sazby jsou vyžadovány, pokud vaše organizace spojuje částky leasingových splátek se sadou indexových sazeb.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f362bf4a6b5de3ce16330aea08880b07b4145792
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992857"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="a2885-104">Nastavení indexových sazeb</span><span class="sxs-lookup"><span data-stu-id="a2885-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2885-105">Pokud leasingové splátky závisí na indexu, lze v systému přidávat a udržovat typy indexových sazeb.</span><span class="sxs-lookup"><span data-stu-id="a2885-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="a2885-106">Pokud chcete přecenit leasingové splátky ze stránky **Typ indexové sazby**, proces přecenění indexové sazby používá nejnovější indexovou sazbu od data přecenění.</span><span class="sxs-lookup"><span data-stu-id="a2885-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="a2885-107">Chcete-li přidat typy indexových sazeb a indexové sazby, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a2885-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="a2885-108">Přejděte na **Majetkový leasing \> Nastavení \> Typ indexové sazby**.</span><span class="sxs-lookup"><span data-stu-id="a2885-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="a2885-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="a2885-109">Select **New**.</span></span>
3. <span data-ttu-id="a2885-110">Do příslušných polí zadejte typ sazby a název indexové sazby.</span><span class="sxs-lookup"><span data-stu-id="a2885-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="a2885-111">Chcete-li přidat novou hodnotu indexové sazby, vyberte typ indexové sazby a poté vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="a2885-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="a2885-112">Vyberte počáteční datum účinnosti sazby a vyberte hodnotu sazby.</span><span class="sxs-lookup"><span data-stu-id="a2885-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="a2885-113">Jako metodu indexové sazby musíte vybrat buď **Rozdíl hodnoty indexové sazby** nebo **Hodnota indexové sazby** .</span><span class="sxs-lookup"><span data-stu-id="a2885-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="a2885-114">Pokud chcete vypočítat novou leasingovou splátku založenou na rozdílu mezi indexovou sazbou k počátečnímu datu a poslední indexovou sazbou, vyberte metodu **Rozdíl hodnoty indexové sazby**.</span><span class="sxs-lookup"><span data-stu-id="a2885-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="a2885-115">Indexová sazba je definována v poli **Indexová sazba (%)**.</span><span class="sxs-lookup"><span data-stu-id="a2885-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="a2885-116">Metodu **Hodnota indexové sazby** vyberte, pokud chcete vypočítat leasingovou splátku pomocí procenta uvedeného v poli **Indexová sazba**.</span><span class="sxs-lookup"><span data-stu-id="a2885-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>
