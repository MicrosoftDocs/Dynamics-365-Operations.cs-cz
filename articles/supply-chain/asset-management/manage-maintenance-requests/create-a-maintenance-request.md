---
title: Vytvořit požadavky na údržbu
description: Tento článek vysvětluje, jak vytvořit požadavek na údržbu v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 92f3a2bc3d2a4d5d1c3be0c6dda2674dc3e7d0bb
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016819"
---
# <a name="create-maintenance-requests"></a>Vytvoření požadavků na údržbu

[!include [banner](../../includes/banner.md)]

 

Požadavky na údržbu lze použít, pokud pracovníci údržby nebo výrobní pracovníci zjistí, že zařízení vyžaduje opravu, ale opravu nelze provést ihned.

**Příklad:** V době, kdy pracovník údržby provádí opravu, zjistí, že je nutné provést servis jiného majetku ve stejném skladovém místě. Pracovník údržby však nemá čas nebo požadované náhradní díly k provedení úlohy opravy. Z tohoto důvodu vytvoří pro majetek požadavek na údržbu a zadá krátký popis výdeje.

Část **Aktivní požadavky na údržbu** v podokně **Související informace** na pravé straně stránky **Všechen majetek** nebo **Aktivní majetek** (**Správa majetku** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**) ukazuje aktivní požadavky na údržbu, které jsou připojeny k vybranému majetku.

1. Vyberte **Správa majetku** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.
2. Zvolte **Nové**.
3. V dialogovém okně **Vytvořit požadavek** vyberte typ požadavku na údržbu v poli **Typ požadavku na údržbu**. Je navržen výchozí typ.
4. Do pole **Popis** zadejte název nebo titul, který stručně popisuje požadavek na údržbu.
5. V polích **Funkční místo** a **Majetek** vyberte podle potřeby funkční místo nebo majetek nebo kombinaci funkčního místa a majetku. Požadavek na údržbu můžete vytvořit bez výběru majetku a majetek lze později přidat do požadavku na údržbu. Pokud pracovník údržby, který je přihlášený, souvisí se zdrojem, který souvisí s majetkem, bude pole **Majetek** nastaveno automaticky.

    Pokud je požadavek na údržbu již připojen k vybranému majetku, zobrazí se v horní části dialogového okna **Vytvořit požadavek** panel zpráv s upozorněním na ID existujícího požadavku na údržbu. Panel zpráv vás také upozorní, když je majetek kryt záruční smlouvou.

6. V poli **Úroveň služby** vyberte úroveň služby označující naléhavost požadavku.
7. Pokud jste v kroku 5 vybrali majetek, můžete vytvořit registraci chyb pomocí polí **Příznak chyby**, **Oblast chyby** a **Typ chyby**.
8. Pokud požadavek na údržbu způsobil výpadek údržby, zadejte počáteční datum a čas prostoje.

    Pole **Zahájil/a** je automaticky nastaveno na vaše jméno.

10. Pole **Skutečný začátek** je automaticky nastaveno na aktuální datum. Hodnotu v tomto poli však můžete podle potřeby měnit.
11. Do pole **Poznámky** zadejte libovolné další požadované poznámky.
12. Vyberte **OK**.

![Vytvořit požadavek na údržbu.](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Následné zpracování požadavků na údržbu

Po vytvoření požadavku na údržbu, ale před jeho převodem na pracovní příkaz, je třeba v něm aktualizovat různé informace. Tento úkol obvykle dokončuje plánovač nebo jiný administrativní zaměstnanec.

- Na stránce **všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** vyberte požadavek, se kterým chcete pracovat, a pak vyberte **Upravit**.

V zobrazení podrobností lze aktualizovat různé informace. Několik příkladů:

- Vyberte a ověřte majetek. Pokud je nutné později vybrat jiný majetek, můžete nastavit možnost **Majetek ověřen** na **Ne**.
- Vyberte odpovědnou skupinu pracovníků údržby nebo odpovědného pracovníka údržby. Další informace o požadovaném nastavení naleznete v části [Zodpovědní pracovníci údržby](../setup-for-maintenance-requests/responsible-workers.md).
- Vyberte typ práce údržby, a pokud jsou tyto informace relevantní, pak příslušnou variantu údržby a odvětví práce.
- Do polí **zeměpisná šířka** a **Zeměpisná délka** zadejte zeměpisné souřadnice. Všechny souřadnice přidané k požadavku na údržby jsou automaticky převedeny do související pracovní objednávky. 

![Aktualizace požadavku na údržbu.](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Pokud při vytváření požadavku na údržbu vyberete určitý majetek, můžete k majetku přidat jednu chybu. Po vytvoření požadavku na údržbu můžete podle potřeby přidat další chyby. Pokud chcete přidat chyby, vyberte **Chyba majetku** na stránce **Všechny požadavky na údržbu**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]