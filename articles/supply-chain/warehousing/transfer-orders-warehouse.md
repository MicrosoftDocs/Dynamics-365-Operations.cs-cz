---
title: Nastavení skladů pro převodní příkazy
description: Toto téma popisuje způsob nastavení skladů pro převodní příkazy.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 7dfb215683b4ee5d186626492bd90116d1a06a1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976831"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Nastavení skladů pro převodní příkazy 

[!include [banner](../includes/banner.md)]

Pomocí úrovní skladů můžete vytvořit hierarchii podporující převodní příkazy mezi sklady. Na základě tohoto nastavení vypočte hlavní plánování požadavky na položky na jedné úrovni skladu a vygeneruje plánované převodní příkazy z přiřazeného zdrojového skladu, aby byly splněny.

1.  Klikněte na možnosti **Řízení zásob > Nastavení > Rozdělení zásob > Sklady**.

2.  Vyberte sklad, který chcete doplnit.

3.  Na pevné záložce **Hlavní plánování** zaškrtněte políčko **Doplnění**.

4.  V poli **Hlavní sklad** vyberte sklad, který chcete přiřadit jako sklad pro doplňování. Hlavní plánování vypočte pro zvolený sklad požadavek na převod a vygeneruje plánovaný převodní příkaz z přiřazeného střediska **Hlavní sklad**.
   
    > [!NOTE]
    > <P>Pokud zrušíte zaškrtnutí políčka <STRONG>Doplňování</STRONG>, bude k vybranému skladu přiřazena úroveň skladu podle hodnoty pole <STRONG>Hlavní sklad</STRONG>, avšak <STRONG>Hlavní sklad</STRONG> nebude nastaven jako doplňovací sklad.</P>

5.  Zavřete stránku k použití nového nastavení.


> [!TIP]
> <P>Chcete-li provést přiřazení určitého skladu pro doplňování, je nutné nejprve daný sklad nastavit jako dimenzi úložiště na stránce <STRONG>Skupiny dimenze úložiště</STRONG>. Na této stránce vyberte pole <STRONG>Aktivní</STRONG> a <STRONG>plán disponibility podle dimenzí</STRONG> pro sklad.</P>

## <a name="set-up-transport-lead-time"></a>Nastavení doby realizace přepravy

Je také nutné nastavit dobu realizace přepravy mezi sklady na stránce **Dny přepravy**. 
1. Přejděte na **Řízení zásob > Nastavení > Distribuce > Dny přepravy**.
2. V poli **Místo příjmu** vyberte **sklad**.
3. Vyberte **odesílající sklad**, **přijímající sklad** a **Počet dnů přepravy**. 
4. (Volitelné) Můžete také nastavit dobu přepravy v závislosti na režimu doručení na kartě **Dny dopravy podle způsobu doručení**.
