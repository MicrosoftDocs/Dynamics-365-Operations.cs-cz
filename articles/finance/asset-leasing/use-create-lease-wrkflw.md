---
title: Použití pracovních postupů schvalování leasingu
description: Toto téma vysvětluje, jak používat pracovní postupy ke schválení leasingu majetku a jak sledovat stav a historii pracovních postupů.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0b35dfa599895cb39cdd6a0a95fdcdcc54c45044
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724918"
---
# <a name="use-lease-approval-workflows"></a>Použití pracovních postupů schvalování leasingu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak používat pracovní postupy ke schválení leasingu majetku a jak sledovat stav a historii pracovních postupů. Pracovní postupy pomáhají zajistit konzistenci správy schválení leasingu poskytnutím standardní sady kroků schválení a přiřazením konkrétních uživatelů, kteří schvalují každý krok procesu. Schvalovatel může schválit leasing, odmítnout ho, požádat o jeho změnu nebo ho přiřadit jinému uživateli ke schválení. Workflovy mohou také více zviditelnit proces schvalování tím, že vám umožní sledovat svůj stav a historii. Dále si můžete prohlédnout centralizovaný pracovní seznam se seznamem úkolů a schválení, která jsou přiřazena konkrétním schvalovatelům.

Než použijete tento postup, ujistěte se, že byl vytvořen alespoň pracovní postup schválení leasingu. Pokud neexistuje žádný pracovní postup, vytvořte jej. Informace o tom, jak nastavit pracovní postup, najdete v části [Použití pracovních postupů schvalování leasingu](set-up-lease-wrkflw.md).

1. Předložte leasing ke schválení. Na stránce **Podrobnosti o rezervaci** pro leasing vyberte **Pracovní postup** a pak vyberte **Odeslat**.
2. V zobrazeném dialogovém okně můžete přidat komentář. Určený schvalovatel uvidí tento komentář spolu s leasingovou smlouvou. Po dokončení zadávání vyberte **Odeslat**. Leasing je odeslán do systému pracovního toku a schvalovatel jej obdrží ke schválení.
3. Chcete-li zobrazit leasingy, které jsou určeny ke schválení, přejděte na **Moduly \> Společný \> Pracovní položky \> Pracovní položky, které mi byly přiděleny**.
4. Na stránce **Pracovní položky, které mi byly přiděleny** vyberte odkaz **ID leasingu** na leasing, který chcete zobrazit. Stránka, která se zobrazí, závisí na knihách leasingu a podrobnostech leasingu, ke kterým máte přístup.
5. Až dokončíte prohlížení leasingu, vyberte **Pracovní postup** a rozhodněte, jaká opatření by měla být přijata. Možnosti zahrnují **Schválit**, **Zamítnout**, **Žádost o změnu**, **Delegát**, a **Zrušeno**. Můžete také vybrat **Zobrazit historii** pro zobrazení historie schválení pro vybraný leasing.
6. Poté, co vyberete akci, zadejte komentář k popisu akce. Po dokončení zadávání komentáře vyberte akci **Schváleno** v seznamu.
7. Chcete-li zobrazit akce schválení, přejděte zpět na stránku **Podrobnosti o leasingu** ze stránky **Souhrn leasingu** a poté vyberte **Pracovní postup \> Zobrazit historii**.

    Aktivity pracovního postupu můžete zobrazit na stránce **Historie pracovního postupu**. Tato stránka zobrazuje kroky pracovního postupu, které byly provedeny při konkrétním leasingu. Můžete také použít pole **Pracovní položky** k zobrazení stavu přiřazených pracovních položek.

8. Chcete-li zastavit pracovní postup, na stránce **Historie pracovního postupu** vyberte **Odvolat**. V dialogovém okně, které se zobrazí, vyberte jinou stránku a pak vyberte **OK**.
9. Chcete-li deaktivovat pracovní postup nebo aktivovat dříve vytvořený pracovní postup, přejděte na **Majetkový leasing \> Nastavení \> Pracovní postup leasingu**. Pak na stránce **Pracovní postup pronájmu** vyberte **Pracovní postup \> Verze**. Chcete-li, aby byl aktuální pracovní postup neaktivní, vyberte v dialogovém okně verze leasingu aktivní leasing a poté vyberte **Neaktivní**. Chcete-li stávající pracovní postup aktivovat, vyberte pracovní postup a poté vyberte **Aktivovat**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
