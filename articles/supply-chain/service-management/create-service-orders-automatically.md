---
title: Automatické vytvoření servisních zakázek
description: Servisní zakázky můžete vytvářet pro jednu nebo více servisních smluv.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 914df1626b02110264b895e82dc9301f3aa0afce
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985111"
---
# <a name="create-service-orders-automatically"></a>Automatické vytvoření servisních zakázek    

[!include [banner](../includes/banner.md)]


Servisní zakázky můžete vytvářet pro jednu nebo více servisních smluv. Po jejich vytvoření můžete servisní zakázky zobrazit ve formuláři **Servisní zakázky** .

Servisní zakázky se vytvářejí pouze pro platné období servisní smlouvy. Jestliže interval, který jste stanovili ve formuláři **Vytvořit servisní zakázky** , spadá do období před počátečním datem nebo po koncovém datu servisní smlouvy, vytvoří se servisní zakázky pouze pro část intervalu, která spadá do intervalu servisní smlouvy.

Pokud ručně nebo automaticky vytváříte servisní zakázky v řádku servisní smlouvy, musí servisní zakázka spadat do časového období, které určuje počáteční a koncové datum definované pro daný řádek. Výjimkou je případ, kdy v řádku neuvedete koncové datum.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Automatické vytvoření servisních zakázek pro servisní smlouvu

1.  Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy** .

2.  Vyberte servisní smlouvu.

3.  Klepněte na kartu **dodat** a klikněte na **plánované servisní zakázky** .

4.  Servisní období určete zadáním dat v polích **Od data** a  **Do data** .

5.  Chcete-li zobrazit seznam servisních zakázek, které jsou vytvořeny, zaškrtněte políčko **Zobrazit informační protokol** .

6.  Vyberte typy transakcí ve skupině polí **Zahrnout typy transakcí** . Typy transakcí představují řádky, které jsou vytvořeny v servisní smlouvě, a každý vybraný typ transakce generuje několik servisních zakázek v závislosti na servisním intervalu stanoveném na řádku servisní smlouvy.

7.  Chcete-li vytvořit libovolné servisní zakázky, které chybějí v souvislé řadě servisních zakázek, zaškrtněte políčko **Nepřetržité** .

8.  Klikněte na tlačítko **OK** .

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Automatické vytvoření servisních zakázek pro několik servisních smluv

1.  Klepněte na tlačítko **řízení servisu** \> **Periodicky** \> **servisní zakázky** \> **Vytvořit servisní zakázky** .

2.  Klepněte na tlačítko **Vybrat** k provedení výběru hodnot, které chcete přidat nebo odebrat při vytváření servisních zakázek.

3.  Klikněte na tlačítko **OK** .

## <a name="see-also"></a>Viz také

[Servisní zakázky](service-orders.md)

[Automaticky vytvářené servisní zakázky](auto-create-service-orders.md)

  


