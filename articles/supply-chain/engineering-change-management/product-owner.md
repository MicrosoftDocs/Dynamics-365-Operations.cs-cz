---
title: Vlastníci produktů
description: Toto téma poskytuje informace o vlastnících produktu. Vlastník produktu je skupina uživatelů, kteří odpovídají za konkrétní produkty. Tyto produkty mohou uvolňovat pouze členové skupiny. Vlastníka produktu lze také použít v pracovním postupu schválení.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4308020d66995d857e547be47216cb82caacf035
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424262"
---
# <a name="product-owners"></a>Vlastníci produktů

[!include [banner](../includes/banner.md)]

Vlastník produktu je skupina uživatelů, kteří odpovídají za konkrétní produkty. Pokud je produktu přiřazena skupina vlastníků produktů, mohou produkt uvolnit pouze členové této skupiny. Vlastníka produktu lze také použít v pracovním postupu schválení ve správě technických změn.

Vlastníci produktů jsou globální nastavení. Proto jsou k dispozici všem právnickým osobám.

## <a name="create-a-product-owner-group"></a>Vytvoření skupiny vlastníků produktů

Chcete-li vytvořit skupinu vlastníků produktů a přidat do ní členy, postupujte takto.

1. Jděte na **Správa technických změn \> Nastavení \> Vlastníci produktu**.
2. V podokně akcí zvolte **Nový**.
3. V poli **Vlastník produktu** zadejte název skupiny.
4. Do pole **Název** zadejte popis skupiny.
5. Na záložce s náhledem **Členové** přidejte pracovníky, kteří by měli být členy skupiny.

## <a name="assign-a-product-owner-to-a-product"></a>Přiřazení vlastníka produktu k produktu

Pokud chcete k produktu přiřadit vlastníka produktu, postupujte takto.

1. Otevřete stránku **Podrobnosti produktu** pro příslušný produkt nebo základní produkt.
1. Na záložce s náhledem **Obecné** nastavte pole **Vlastník produktu** na název příslušné skupiny vlastníků produktů.

Zatímco je vlastník produktu přiřazen k produktu, mohou nastavení **Vlastník produktu** upravovat pouze členové skupiny vlastníků produktu.

Vlastník produktu je také viditelný na stránce **Uvolněné produkty**.

## <a name="product-owners-and-product-releases"></a>Vlastníci produktů a uvolnění produktů

Tento produkt mohou uvolnit pouze uživatelé ze skupiny vlastníků produktů. Existuje však výjimka, když je produkt podřízenou položkou a jeho nadřazená položka je uvolněna vlastníkem nadřazené položky. Jinými slovy, pokud je produkt součástí kusovníku jiného produktu, systém nekontroluje vlastníka produktu každé položky v kusovníku. Kontroluje pouze vlastníka produktu nadřazené položky.

Například produkt X je přiřazen ke skupině vlastníků produktu *Designové skříňky*. Produkt X je také součástí kusovníku produktu Y, který je přiřazen ke skupině vlastníků produktů *Designové reproduktory*. Pokud uživatel ze skupiny vlastníků produktů *Designové reproduktory* uvolňuje produkt Y a jeho kusovník, produkt X bude uvolněn společně s produktem Y.

## <a name="product-owners-and-approvals"></a>Vlastníci produktů a schválení

Protože vlastníci produktů vědí, zda konkrétní technické změny budou pro jejich produkty přínosem, má často smysl je zahrnout jako součást schvalovacího procesu do správy technických změn. Tento přístup můžete implementovat nastavením vlastníků produktů jako poskytovatelů účastníků v pracovních postupech, které se používají pro správu technických změn. Systém poté přiřadí úkoly schválení v pracovních postupech na základě produktů, které jsou v požadavcích na technické změny a příkazech k technickým změnám. Další informace naleznete v tématu [Správa změn technických produktů](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]