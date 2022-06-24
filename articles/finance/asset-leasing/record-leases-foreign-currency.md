---
title: Záznam leasingů v cizích měnách
description: Tento článek vysvětluje, jak zaznamenávat leasingy v jiných měnách, než je měna účetnictví nebo vykazování.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 56c15e648d6aa515192a6f41ba06df6405ca79f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878095"
---
# <a name="record-leases-in-foreign-currencies"></a>Záznam leasingů v cizích měnách

[!include [banner](../includes/banner.md)]

Majetkové leasingové účty pro leasingy, které jsou v jiných měnách než v účetní měně nebo měně vykazování, jsou stanoveny na stránce **Nastavení hlavní knihy**. Všechny leasingy by měly být zadány v měně transakce. Jinými slovy, měly by být zadány v měně uvedené v leasingové smlouvě. Tento článek vysvětluje, jak zaznamenávat leasingy v jiných měnách, než je měna účetnictví nebo vykazování.

Pokud zadáte leasing v cizí měně, používaný majetek se odepisuje jak v účetní měně, tak v měně vykazování. Tyto měny jsou konfigurovány na stránce **Nastavení hlavní knihy**. Toto chování se také používá u dlouhodobého majetku. Když vytvoříte leasing v cizí měně, vyberte měnu transakce v poli **Měna**.

Směnný kurz účetní měny je výchozí hodnota v poli **Směnný kurz účetní měny**. Směnný kurz měny vykazování je výchozí hodnota v poli **Směnný kurz měny vykazování**. Tyto směnné kurzy byly účinné k datu zahájení leasingu. Pole **Směnný kurz účetní měny** a **Směnný kurz měny vykazování** jsou na pevné záložce **Finanční informace a informace o výměně zpráv** na stránce **Podrobnosti o pronájmu**.

1. Zaškrtněte políčko **Pevná sazba**, pokud chcete přepsat směnný kurz, který byl automaticky zadán, a poté zadejte nový kurz.
2. V ostatních polích zadejte informace, které jsou vyžadovány pro leasing, a poté vyberte **Vytvořit plány**.
3. Na nové stránce **Podrobnosti o leasingu** vyberte **Knihy**.
4. Na stránce **Leasingová kniha** na kartě **Finanční informace a informace o měně vykazování** ověřte hodnoty polí **Účetní měna počátečního používaného majetku** a **Měna vykazování počátečního používaného majetku**. Každé z těchto polí zobrazuje přeložený zůstatek používaného majetku v odpovídající měně. Tato pole se aktualizují vždy, když změníte jakékoli finanční informace. Vyberte **Vytvořit plány**, než potvrdíte časový plán plateb.

    Položka deníku prvotního uznání zaznamenává používaný majetek, který používá směnné kurzy uvedené v leasingu. Položka deníku zahrnuje také hodnoty polí **Účetní měna počátečního používaného majetku** a **Měna vykazování počátečního používaného majetku**.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Následné ocenění pro leasingy v cizí měně

Odpisový plán zobrazuje očekávané částky odpisových nákladů v měně vykazování, měně účetnictví a měně transakce.

Chcete-li zobrazit zůstatky používaného majetku a částky odpisů buď v měně vykazování, nebo v účetní měně, otevřete stránku **Odpisový plán majetku** a zaškrtněte políčko **Zobrazit částky v účetní měně** nebo **Zobrazit částky ve vykazované měně**.

Když vytvoříte položky deníku odpisů proti leasingu denominovanému v cizí měně, použije položka směnné kurzy uvedené v leasingu. Použije také hodnoty polí **Účetní měna počátečního používaného majetku** a **Měna vykazování počátečního používaného majetku**.

Konečnou částku odpisových výdajů lze vypočítat pomocí mírně odlišného směnného kurzu, takže používaný majetek je plně odepsán jak v účetní měně, tak v měně vykazování.

Pokud byl leasing překlasifikován na **Odložený nájem**, systém automaticky vymaže směnné kurzy účetní měny a měny vykazování, pokud již byly definovány.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
