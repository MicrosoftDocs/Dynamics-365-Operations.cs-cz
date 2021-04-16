---
title: Nastavení indexových sazeb
description: Toto téma vysvětluje, jak nastavit indexové sazby. Indexové sazby jsou vyžadovány, pokud vaše organizace spojuje částky leasingových splátek se sadou indexových sazeb.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6424248e8d01d04720ad65e80aaa543b42abccc6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823016"
---
# <a name="set-up-index-rates"></a>Nastavení indexových sazeb

[!include [banner](../includes/banner.md)]

Pokud leasingové splátky závisí na indexu, lze v systému přidávat a udržovat typy indexových sazeb. Pokud chcete přecenit leasingové splátky ze stránky **Typ indexové sazby**, proces přecenění indexové sazby používá nejnovější indexovou sazbu od data přecenění.

Chcete-li přidat typy indexových sazeb a indexové sazby, postupujte takto.

1. Přejděte na **Majetkový leasing \> Nastavení \> Typ indexové sazby**.
2. Zvolte **Nové**.
3. Do příslušných polí zadejte typ sazby a název indexové sazby.
4. Chcete-li přidat novou hodnotu indexové sazby, vyberte typ indexové sazby a poté vyberte **Přidat**.
5. Vyberte počáteční datum účinnosti sazby a vyberte hodnotu sazby.

Jako metodu indexové sazby musíte vybrat buď **Rozdíl hodnoty indexové sazby** nebo **Hodnota indexové sazby** .

- Pokud chcete vypočítat novou leasingovou splátku založenou na rozdílu mezi indexovou sazbou k počátečnímu datu a poslední indexovou sazbou, vyberte metodu **Rozdíl hodnoty indexové sazby**. Indexová sazba je definována v poli **Indexová sazba (%)**.
- Metodu **Hodnota indexové sazby** vyberte, pokud chcete vypočítat leasingovou splátku pomocí procenta uvedeného v poli **Indexová sazba**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]