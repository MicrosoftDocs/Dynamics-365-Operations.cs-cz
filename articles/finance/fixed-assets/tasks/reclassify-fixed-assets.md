---
title: Přeřazení dlouhodobého majetku
description: Tento článek vysvětluje proces překlasifikování majetku. Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bd901b1709f0b006cecfbbf6d8c170b56f89d19
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284356"
---
# <a name="reclassify-fixed-assets"></a>Přeřazení dlouhodobého majetku

[!include [banner](../../includes/banner.md)]

Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo. 

Když je dlouhodobý majetek reklasifikován:

- Pro nový dlouhodobý majetek budou vytvořeny všechny knihy pro existující dlouhodobý majetek. Veškeré informace nastavené pro původní dlouhodobý majetek se zkopírují do nového dlouhodobého majetku. Stav knih původního dlouhodobého majetku je Zavřeno. 

- Nové knihy nového dlouhodobého majetku budou mít v poli **Datum pořízení** uvedeno datum reklasifikace. Datum v poli **Datum zahájení odpisu** bude zkopírováno z původních informací o majetku. Pokud již byl zahájen odpis, zobrazí se v poli **Datum posledního odpisu** datum reklasifikace. 

- Existující transakce dlouhodobého majetku pro původní dlouhodobý majetek jsou zrušeny a opětovně vytvořeny pro nový dlouhodobý majetek.

- Když je majetek, který má transakci převodu, překlasifikován, systém zobrazí zprávu v možnosti **Centrum akcí** k označení, že transakce převodu nebyla dokončena během procesu reklasifikace. Je nutné dokončit transakci převodu, abyste přesunuli existující transakce reklasifikace do příslušných finančních dimenzí. 

   Během procesu reklasifikace provede systém následující akce, které reklasifikují zůstatek majetku z původního na nový. 
   
   - Proces reklasifikace zkopíruje data z původní knihy dlouhodobého majetku do nové knihy dlouhodobého majetku.

   - Transakce reklasifikace používá informace z původní zaúčtované akvizice, které zahrnují informace o finanční dimenzi, které jsou zahrnuty v transakci pořízení.  
   
   - Proces reklasifikace zároveň obrací původní transakci pořízení a transakci převodu majetku. 

Následující diagram a postup poskytují příklad procesu reklasifikace. 

[![Schéma znázorňující proces reklasifikace.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Chcete-li reklasifikovat dlouhodobý majetek, postupujte takto:

1. Přejděte na **Dlouhodobý majetek > Pravidelné úlohy > Reklasifikace.**
2. V poli **Skupina dlouhodobého majetku** zvolte skupinu, která má být reklasifikována.
3. V poli **Číslo dlouhodobého majetku** zvolte dlouhodobý majetek určený k reklasifikaci.
4. V poli **Nová skupina dlouhodobého majetku** vyberte skupinu, do které chcete dlouhodobý majetek převést.
    * Jestliže je nová skupina dlouhodobého majetku přiřazena k číselné řadě, pole **Nové číslo dlouhodobého majetku** se aktualizuje číslem z číselné řady nové skupiny dlouhodobého majetku. V opačném případě se pole **Nové číslo dlouhodobého majetku** aktualizuje číslem z číselné řady, která je nastavena na stránce **Parametry dlouhodobého majetku**. Pokud na stránce **Parametry dlouhodobého majetku** není nastavena číselná řada, zadejte číslo do pole **Nové číslo dlouhodobého majetku**.  
5. Do pole **Datum reklasifikace** zadejte datum.
6. V poli **Číselná řada dokladů** zadejte nebo vyberte hodnotu.
7. Vyberte **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
