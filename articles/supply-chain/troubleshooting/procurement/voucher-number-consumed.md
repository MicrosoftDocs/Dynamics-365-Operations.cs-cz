---
title: Číslo poukazu o přijetí produktu je spotřebováno, i když není generován poukaz
description: Číslo dokladu příjemky produktu je spotřebováno, i když se během příjmu produktu nevygeneruje žádný finanční doklad
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475790"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Číslo poukazu o přijetí produktu je spotřebováno, i když není generován poukaz

## <a name="symptoms"></a>Příznaky

Číslo dokladu příjemky produktu je spotřebováno, i když se během příjmu produktu nevygeneruje žádný finanční doklad.

## <a name="resolution"></a>Řešení

Pokud je možnost **Časově rozlišit pasiva na příjemce produktu** nastavena na *Ne* pro skupinu modelů položek, nedojde k účtování do hlavní knihy. Fyzická událost však bude zaznamenána pro účely účtování v dílčí hlavní knize a tato událost vyžaduje číslo dokladu. Toto číslo dokladu je číslo dokladu, na které se odkazuje v transakcích zásob.

Doporučujeme nastavit možnost **Časově rozlišit pasiva na příjemce produktu** na *Ano*, jak je popsáno v následujícím příspěvku na blogu: [Zaúčtování vedlejších nákladů v době příjemky produktu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
