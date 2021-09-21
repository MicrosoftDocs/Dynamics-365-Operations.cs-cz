---
title: Pokud je vydání prázdné a je povolen prázdný příjem, nelze přesunout registrační značku
description: Pokud je sériové číslo prázdné a je povolen prázdný příjem, nemůžete přesunout registrační značku. To bude opraveno tím, že pole sériového čísla bude volitelné.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475788"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Pokud je sériové číslo prázdné a je povolen prázdný příjem, nelze přesunout registrační značku

## <a name="symptoms"></a>Příznaky

Registrační značku nelze přesunout pomocí položky nabídky **Přesun**, pokud má sériové číslo nastavení *Prázdný výdej povolen* a *Prázdná příjemka povolena* ve skupině dimenze sledování a pokud je na stejném místě více registračních značek, některé mají sériová čísla a některé ne.

## <a name="resolution"></a>Řešení

Tento problém bude vyřešen změnami, které jsou nasazeny v [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Tyto změny způsobí, že je pole **Sériové číslo** nepovinné, pokud jsou povoleny prázdné příjemky a prázdné výdeje.
