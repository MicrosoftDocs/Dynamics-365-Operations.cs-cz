---
title: Časové rozlišení předplatného
description: U předplatného servisu ručně rozlišujete výnosy do období následujících po datu, kdy jste fakturovali transakci poplatku.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ff184b24a264e37613b2302a3d92b74e870c5ac
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677331"
---
# <a name="accruing-subscriptions"></a>Časové rozlišení předplatného 

[!include [banner](../includes/banner.md)]


U předplatného servisu ručně rozlišujete výnosy do období následujících po datu, kdy jste fakturovali transakci poplatku.

Období časového rozlišení jsou vytvořena pro pro fakturační období, které jste nastavili pro poplatek předplatného, a jsou založena na kódu období předplatného.

Můžete provádět časové rozlišení a stornovat časově rozlišené výnosy.

## <a name="reverse-accruals-of-credit-amounts"></a>Stornovat časové rozlišení v částkách kreditu

Při připsání fakturovaných částek předplatného na stranu Dal můžete použít dvě metody stornování časově rozlišených částek:

  - Před vytvořením návrhu dobropisu pro transakci můžete stornovat každou transakci časového rozlišení výnosů zvlášť. Toto je ruční metoda. (ruční)

  - Můžete časově rozlišené částky stornovat k datu zaúčtování dobropisu nebo k původnímu datu zaúčtování časového rozlišení.

Další informace naleznete v tématu [Parametry předplatného (formulář)](/dynamicsax-2012//subscription-parameters-form).

## <a name="setup-requirements"></a>Nastavit požadavky

Chcete-li časově rozlišovat výnosy, ověřte, zda jsou splněny následující datové požadavky:

## <a name="account-setup"></a>Nastavení účtu

V modulu **Project** musí být nastaveny účty **Časově rozlišený výnos – předplatné** a **NV – předplatné**.

Při zaúčtování časově rozlišeného výnosu se časově rozlišená částka připíše na stranu MD účtu **Nedokončená výroba - předplatné** a časově rozlišená částka na stranu Dal účtu **Časově rozlišené výnosy – předplatné**.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Nastavení účtů pro časové rozlišení výnosu předplatného

1.  Klepněte na tlačítko **Řízení a účetnictví projektu** \> **Nastavení** \> **Zaúčtování** \> **Nastavení zaúčtování v hlavní knize**.

2.  Klepněte na kartu **Výnosové účty** a vyberte **nedokončená výroba – předplatné** nebo **časově rozlišené výnosy – předplatné** k nastavení účtů.

## <a name="subscription-group-setup"></a>Nastavení skupiny předplatného

Aby bylo možné časově rozlišovat výnosy předplatného, musí být zaškrtnuto políčko **časově rozlišené výnosy**. Nachází se ve formuláři **skupiny předplatného** skupiny, která je připojena k předplatnému. Klikněte na uzel **Řízení služeb** \> **Nastavení** \> **Servisní zakázky** \> **Skupiny předplatného**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Povolení časového rozlišení výnosů u skupiny předplatného

Klikněte na uzel **Řízení služeb** \> **Nastavení** \> **Servisní zakázky** \> **Skupiny předplatného**.

## <a name="periods"></a>Období

Musíte nastavit kód fakturačního období. Pokud nechcete časově rozlišovat výnosy ve stejných časových obdobích, která používáte k fakturaci, musíte rovněž nastavit období časového rozlišení.

V následující tabulce získáte přehled o možných obdobích časového rozlišení, která lze nastavit pro různá fakturační období:

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Fakturační období</p></th>
<th><p>Období časového rozlišení</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Roky</strong></p></td>
<td><ul>
<li><p><strong>Roky</strong></p></li>
<li><p><strong>Čtvrtletí</strong></p></li>
<li><p><strong>Měsíc</strong></p></li>
<li><p><strong>Den</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Čtvrtletí</strong></p></td>
<td><ul>
<li><p><strong>Čtvrtletí</strong></p></li>
<li><p><strong>Měsíc</strong></p></li>
<li><p><strong>Den</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Měsíc</strong></p></td>
<td><ul>
<li><p><strong>Měsíc</strong></p></li>
<li><p><strong>Den</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Týden</strong></p></td>
<td><ul>
<li><p><strong>Den</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Den</strong></p></td>
<td><ul>
<li><p><strong>Den</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Nastavení fakturačního období je povinnou součástí celého nastavení skupiny předplatného. Můžete se rozhodnout, zda chcete také nastavit období časového rozlišení pro skupinu předplatného. Pokud nastavíte období časového rozlišení pro skupinu předplatného ,je toto období navrženo v poli **Kód období**. Toto pole se nachází ve formuláři **časově rozlišené výnosy předplatného** při časovém rozlišení výnosů předplatného. Období časového rozlišení je však nepovinná informace o skupině předplatného.


> [!NOTE]
> <P>K otevření formuláře <STRONG>Časové rozlišení předplatného</STRONG> použijte následující cestu. Klikněte na uzel <STRONG>Řízení služeb</STRONG> &gt; <STRONG>Pravidelné</STRONG> &gt; <STRONG>Servisní odběry</STRONG> &gt; <STRONG>Všechna předplatná služby</STRONG>.</P>


## <a name="transactions"></a>Transakce

Můžete určit počet transakcí hlavní knihy, které jsou vytvořeny při zaúčtování časově rozlišeného výnosu. U předplatného definujte, zda transakce hlavní knihy mají být vytvořeny jako celek nebo podle řádku.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Určení úrovně zobrazovaných podrobností o zaúčtování pro časově rozlišené transakce

1.  Klikněte na **Řízení a účetnictví projektů** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.

2.  Na kartě **Finanční** v poli **Faktura** vyberte **Celkem** nebo **řádek**.


## <a name="see-also"></a>Viz také

[Časově rozlišit výnosy z předplatného](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]