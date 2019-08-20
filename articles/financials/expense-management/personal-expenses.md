---
title: Osobní výdaje ve vyúčtování výdajů
description: Toto téma vysvětluje dvě metody pro zpracování osobních výdajů zaměstnance v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794975"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="1adc6-103">Osobní výdaje v sestavě výdajů</span><span class="sxs-lookup"><span data-stu-id="1adc6-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1adc6-104">Během služební cesty může dojít k tomu, že zaměstnanec zaplatí osobní výdaje kreditní kartou společnosti.</span><span class="sxs-lookup"><span data-stu-id="1adc6-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="1adc6-105">Pokud není definovaný proces pro osobní výdaje, může být schválení vyúčtování výdajů přerušeno, když zaměstnanec odevzdá rozpis vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="1adc6-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="1adc6-106">V aplikaci Microsoft Dynamics 365 for Finance and Operations existují dvě metody pro zpracování osobních výdajů zaměstnance:</span><span class="sxs-lookup"><span data-stu-id="1adc6-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="1adc6-107">**Zaplaceno zaměstnancem** – Vaše organizace neplatí osobní výdaje, které se objevují na výpisu platební karty společnosti.</span><span class="sxs-lookup"><span data-stu-id="1adc6-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="1adc6-108">Místo toho se vytváří sestava zobrazující osobní výdaje společně s firemními výdaji, které byly zaúčtovány na platební kartu společnosti.</span><span class="sxs-lookup"><span data-stu-id="1adc6-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="1adc6-109">**Placené společností** – Společnost proplatí všechny položky na výpisu z kreditní karty a potom zatíží účet pracovníka částkou osobních výdajů.</span><span class="sxs-lookup"><span data-stu-id="1adc6-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="1adc6-110">Na stránce **Parametry správy výdajů** můžete vybrat metodu, kterou používá vaše organizace.</span><span class="sxs-lookup"><span data-stu-id="1adc6-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
