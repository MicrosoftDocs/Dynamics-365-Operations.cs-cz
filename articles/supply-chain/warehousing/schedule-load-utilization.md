---
title: Naplánovat využití vytížení
description: Toto téma vysvětluje postup při nastavení a plánování vytížení v určitém skladu.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac4dcba153b8da3d62261326c3c4e169325c2210
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977381"
---
# <a name="schedule-load-utilization"></a>Naplánovat využití vytížení

[!include[banner](../includes/banner.md)]

Můžete naplánovat zatížení využití typů vybraného umístění a také projektovat současné i budoucí využití zatížení. Může projektovat vytížení jednoho nebo více míst, pro měrné zatížení jednotek (zóna nebo sklad) nebo kombinace zóny a skladu.

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a>Plánování a zobrazení zatížení pro sklad nebo místo

Chcete-li naplánovat zatížení míst, skladů nebo zón, vytvořte nastavení využití prostoru a přidružte ho s hlavním plánem.

V nastavení využití místa, můžete použít typy skladových míst, například **Hromadná umístění** a **výdejní skladové místo** k určení, jak by mělo být využití místa naplánováno. Můžete také určit režimu vytížení skladu, jako například **Pásmo**.

Projekte budoucího využití místa vychází z informací, které se počítají z přidruženého hlavního plánu. Hlavní plány předpovídají plánování zdrojů pro příchozí a odchozí příkazy pro výrobu a operace. Projekce volného místa je založena na vztahu mezi nastavením využití prostoru a vybraným hlavním plánem.

Pomocí režimu vytížení jednotky zvolené v nastavení využití prostoru určíte, zda vytížení by mělo být plánované pro každý sklad nebo zónu nebo zda má projektování zahrnovat informace o skladu i o zóně. Můžete také určit, zda by blokovaná umístění měla být vyloučena z výpočtů pro využití zatížení.

Využití místa lze projektovat generováním sestavy **využití vytížení skladu**. Při generování sestavy můžete určit, zda se využití vytížení má projektovat pro každé místo, pro všechny místa nebo pro vybrané jednotky vytížení, například pásmo nebo sklad.

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a>Tvorba nastavení využití prostorů pro sklad

1. Vyberte **řízení zásob** \> **nastavení** \> **sledování skladu** \> **Využití místa**.
2. Chcete-li vytvořit nastavení využití místa, klikněte na položku **Nové**. Zadejte ID a název pro nové nastavení.
3. V poli **Režim vytížení skladu** vyberte, zda by měl přehled využití místa určován podle skladu, zóny, nebo skladu a zóny.
4. Nastavte možnost **vyloučit blokován umístění** na **Ano** k vyloučení blokovaných skladových míst z výpočtu volného místa. Skladové místo můžete blokovat pro vstup a výstup určením důvodu blokování v poli **Blokovaný vstup** nebo **Blokovaný výstup** na pevné záložce **Jiné** na stránce **Skladovací místa**.
5. Na pevné záložce **Typ místa** vyberte typy umístění, které chcete zahrnout do výpočtu využití prostoru. Je nutné vybrat alespoň jeden typ umístění pro projektování.

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a>Přidružte nastavení využití prostoru hlavního plánu

1. Vyberte **Řízení zásob** \> **Periodické úkoly** \> **Naplánovat využití vytížení**.
2. V poli **hlavní plán** vyberte hlavní plán.
3. V poli **Počet dní** zadejte počet dní, které chcete zahrnout do projektování aktuálního a budoucího pracovního vytížení.
4. V poli **Využití místa** vyberte nastavení využití místa pro projektování aktuálního a budoucího pracovního vytížení.

### <a name="specify-the-load-utilization-projection-and-view-information"></a>Zadejte informace o projektování a zobrazení vytížení využití

1. Vyberte **řízení zásob** \> **dotazy a sestavy** \> **sestavy fyzických zásob** \> **využití vytížení skladu**.
2. V poli **Zobrazit podle** vyberte úroveň projektování využití prostoru:

    - **Web** – Projekt k projektování využití prostoru pro každé místo. Toto projektování je užitečné, pokud například chcete zobrazit všechny sklady v místě, takže můžete vyrovnávat využití prostoru mezi sklady.
    - **Jednotka vytížení** – projekt k projektování využití prostoru zón či skladů. Dostupné místo je poté projektované podle hodnoty, kterou jste vybrali v poli **režim vytížení úložiště** na stránce **využití místa** při vytváření nastavení využití místa.

3. Proveďte některý z následujících kroků v závislosti na hodnotě, kterou jste vybrali v předchozím kroku:

    - Pokud jste vybrali v poli **Zobrazit podle** možnost **Web**, bude k dispozici pole **Web**. Vyberte jedno nebo více pracovišť, které chcete zahrnout do projektování.
    - Pokud jste vybrali v poli **Zobrazit podle** možnost **Jednotka vytížení**, bude k dispozici pole **Jednotka vytížení**. Vyberte jednotku vytížení.

4. V poli **Typ vytížení** vyberte **Objem** nebo **Hmotnost** pro označení provozní jednotky skladu, pro který se má projektovat prostor.
5. V poli **Nastavení využití prostoru** vyberte nastavení využití prostoru, na kterém by mělo být projektování založeno.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]