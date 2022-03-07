---
title: Šablony servisu
description: Můžete definovat servisní smlouvu jako šablonu a později můžete zkopírovat řádky této šablony do jiné servisní smlouvy nebo do servisní zakázky.
author: kamaybac
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82a19dbee91f13eb3ef56dfd67a775930170b8e7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576297"
---
# <a name="service-templates"></a>Šablony servisu

[!include [banner](../includes/banner.md)]

Můžete definovat servisní smlouvu jako šablonu a později můžete zkopírovat řádky této šablony do jiné servisní smlouvy nebo do servisní zakázky.

## <a name="example"></a>Příklad

Předpokládejme, že odběratel, pro kterého poskytujete služby, má stejné služební výtahy v pěti různých sídlech.

Pro tohoto odběratele je třeba vytvořit pět servisních smluv, jednu pro každé sídlo.
Chcete-li omezit opakující se úkony konfigurace a přitom zajistit, že konfigurační údaje v servisních smlouvách budou shodné, vytvořte servisní smlouvu a specifikujte ji jako šablonu pro servisní práce na výtazích.

Nyní můžete zkopírovat řádky šablony do pěti nových servisních smluv, takže každá servisní smlouva bude zaplněna řádky ze šablony.

## <a name="create-a-template"></a>Vytvořit šablonu

Při vytváření servisní šablony nejprve vytvořte servisní smlouvu, poté pro ni vytvořte povinné řádky a nakonec servisní smlouvu přiřaďte ke skupině servisních šablon.

> [!NOTE]
> Servisní smlouvu lze definovat jako šablonu pouze tehdy, pokud k ní nejsou připojeny žádné servisní zakázky. Kromě toho nelze ze servisní smlouvy, která byla definována jako šablona, vygenerovat žádné servisní zakázky.

## <a name="copy-template-lines"></a>Kopírovat řádky šablony

Řádky šablony lze kopírovat ze servisní šablony do jiné servisní smlouvy nebo do servisní objednávky.

Pokud kopírujete řádky šablony do servisních objednávek nebo servisních smluv, budou odpovídající skupiny šablon zobrazeny v zobrazení stromu, v němž lze jednotlivé skupiny rozbalit. V tomto zobrazení lze zobrazit každou šablonu a řádek šablony.

Při seskupení šablon s použitím názvů odpovídajících použití těchto šablon lze snáze určit, které řádky servisní šablony mají být zkopírovány.

## <a name="related-topics"></a>Související témata

[Kopírování řádků šablon servisu](copy-service-template-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]