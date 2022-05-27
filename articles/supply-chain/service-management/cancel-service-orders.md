---
title: Zrušit servisní zakázky
description: Servisní zakázku nebo řádek servisní zakázky můžete zrušit z dané servisní zakázky, více servisních zakázek můžete zrušit spuštěním periodické úlohy.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e75ed6e30ece1f4807ff036d831c269774d941a7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670965"
---
# <a name="cancel-service-orders"></a>Zrušit servisní zakázky   

[!include [banner](../includes/banner.md)]


Servisní zakázku nebo řádek servisní zakázky můžete zrušit z dané servisní zakázky, více servisních zakázek můžete zrušit spuštěním periodické úlohy.


> [!NOTE]
> <P>Servisní zakázky nelze zrušit v případě, že fáze servisní zakázky neumožňuje zrušení, pokud servisní zakázka obsahuje požadavky na položky nebo pokud již byla servisní zakázka zaúčtována.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Zrušení servisní zakázky ve formuláři Servisní zakázky

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**. Vyberte webovou servisní zakázku a v podokně akcí klikněte na **Zrušit objednávku**.

## <a name="cancel-a-service-order-line"></a>Zrušení řádku servisní zakázky

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**. V dolním podokně dvakrát klikněte na řádek servisní zakázky, který chcete zrušit.

2.  Vyberte řádek servisní zakázky, kterou chcete zrušit, a klepněte na tlačítko **Zrušit řádek objednávky** ke změně stavu řádku na **zrušeno**.


> [!TIP]
> <P>Chcete-li odvolat zrušení řádku servisní zakázky a změnit stav zpět na <STRONG>vytvořeno</STRONG>, klepněte na tlačítko <STRONG>odvolat zrušení</STRONG>.</P>


## <a name="cancel-multiple-service-orders"></a>Zrušení více servisních zakázek

1.  Klepněte na tlačítko **řízení servisu** \> **Periodicky** \> **servisní zakázky** \> **Zrušit servisní zakázky**.

2.  Klikněte na tlačítko **Vybrat**.

3.  Ve formuláři **Dotaz** ve sloupci **Kritéria** vyberte servisní zakázky, které chcete zrušit.

4.  Klepnutím na tlačítko **OK** zavřete formulář **Dotaz**.

5.  Jestliže chcete generovat informační protokol, který zobrazí zrušené servisní zakázky, zaškrtněte políčko **Zobrazit informační protokol**.

6.  Chcete-li odvolat stav **Zrušené** servisní zakázky, zaškrtněte políčko **Odvolat storno**.

7.  Klikněte na tlačítko **OK**.

Vybrané servisní zakázky budou buď zrušeny, nebo bude jejich stav **Zrušeno** odvolán na stav **Zpracovává se**.


> [!NOTE]
> <P>Pokud zaškrtnete políčko <STRONG>Odvolat zrušení</STRONG>, servisní zakázky se stavem <STRONG>Zrušeno</STRONG> budou vráceny zpět a stav <STRONG>Zpracovává se</STRONG> nebude zrušen.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]