---
title: Nastavení dispozičních kódů
description: Tento postup se zaměřuje na nastavení dispozičního kódu, který lze použít v mobilním zařízení pro proces příjmu vratky.
author: Mirzaab
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb83108c934e864da0df39ec4ee36a0bc7ba7588
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574058"
---
# <a name="set-up-dispositions-codes"></a>Nastavení dispozičních kódů

[!include [banner](../../includes/banner.md)]

Tento postup se zaměřuje na nastavení dispozičního kódu, který lze použít v mobilním zařízení pro proces příjmu vratky. Dispoziční kódy je sada pravidel, které lze použít při příjmu položek. Například když uživatel při práci používá mobilní zařízení k příjmu položek, které byly poškozené, uživatel musí naskenovat dispoziční kód pro poškozené položky. Podle naskenovaného dispozičního kódu lze určit stav zásob přijatého zboží, šablonu práce a směrnici umístění. Pro proces Příjem nákupní objednávky a Vykázat výrobní zakázku jako dokončenou lze dispoziční kód použít volitelně. Pokud v případě procesu příjmu prodejní vratky jsou položky registrovány pomocí mobilního zařízení, použití dispozičního kódu je povinné.  Tento průvodce byl vytvořen pomocí ukázkových dat společnosti USMF. Tento postup je určen pro vedoucího skladu. 

1. Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Dispoziční kódy.
2. Klikněte na položku Nová.
    * Vytvořte nový dispoziční kód pro použití u vrácených položek odběratele.  
3. Zadejte hodnotu do pole Dispoziční kód.
4. V poli Stav zásob vyberte stav zásob v případě, že existuje blokování zásob.
    * V případě, že používáte USMF, vyberte „Blokování“. K dispozičnímu kódu můžete přidat stav zásob, a tak přepsat výchozí stav na řádcích objednávky.  
5. Zadejte hodnotu do pole Šablona práce.
    * Volitelné: Vyberte kód šablony práce přidružený k vratce. Jestliže není zadána žádná hodnota, bude šablona práce přeložena pomocí standardních pravidel nastavených v systému. Výběr šablony práce omezí procesy, se kterými lze tento dispoziční kód použít. Například pokud má dispoziční kód šablonu práce s pracovním příkazem typu nákupní objednávky, nelze jej použít k registraci položek vrácených odběratelem.  
6. Zadejte hodnotu do pole Vrátit dispoziční kód.
    * Dispoziční kód vrácení určuje zbývající proces vratky pro registrované položky. V tomto příkladu by měl odběratel obdržet dobropis. Přidejte dispoziční kód vrácení obsahující akci Dal.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]