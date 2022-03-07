---
title: Nastavení zařízení pro spuštění rozhraní pro provádění výrobního provozu
description: Rozhraní pro provádění výrobního provozu je nastaveno pro každé zařízení ve výrobním provozu. Společnosti obvykle nastavují každé zařízení odlišně v závislosti na účelu, kterému zařízení slouží. Společnost může mít například jedno zařízení v recepci, kde pracovníci registrují příchod a odchod, a další v dílně, kde pracovníci spravují stanovené úkoly.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 34e29a43cebeec16357aecb036c534da35820d90ae602d67419a9606afc542ee
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735961"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Nastavení zařízení pro spuštění rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Rozhraní pro provádění výrobního provozu je nastaveno pro každé zařízení ve výrobním provozu. Společnosti obvykle nastavují každé zařízení odlišně v závislosti na účelu, kterému zařízení slouží. Společnost může mít například jedno zařízení v recepci, kde pracovníci registrují příchod a odchod, a další v dílně, kde pracovníci spravují stanovené úkoly.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Nastavení konfigurace a filtrů pro konkrétní zařízení

Chcete-li nastavit konfiguraci a filtry úloh pro zařízení, přihlaste se na stránce **Provádění výrobního provozu** pomocí účtu, který má roli zabezpečení zahrnující funkční oprávnění *Supervizor doby údržby*. (Mezi dodávanými rolemi zabezpečení má tohle funkční oprávnění pouze *Vedoucí dílny*.) Poté postupujte podle těchto kroků.

1. Přejděte na zařízení, které chcete nastavit, a přihlaste se k Microsoft Dynamics 365 Supply Chain Management jako vedoucí dílny. (Použijte účet, který obsahuje funkční oprávnění *Supervizor doby údržby*.)
1. Ujistěte se, že je k dispozici konfigurace pro zařízení, které nastavujete. Pokud ještě žádná konfigurace neexistuje, je k dispozici výchozí konfigurace. Další informace o nastavení konfigurace najdete v části [Konfigurace rozhraní pro provádění výrobního provozu](production-floor-execution-configure.md).
1. Přejděte do nabídky **Řízení výroby \> Provádění výroby \> Provádění výrobního provozu**.

    Pokud již bylo na aktuálním zařízení alespoň jednou nakonfigurováno rozhraní pro provádění výrobního provozu, zobrazí se přihlašovací stránka. Jinak se zobrazí uvítací stránka.

1. Na přihlašovací stránce nebo na uvítací stránce vyberte **Konfigurovat**.
1. V seznamu vyberte konfiguraci.
1. Zvolte **Další**.
1. Vyberte jeden nebo více filtrů, které chcete použít na aktuální zařízení. Tyto filtry pomohou zajistit, aby se na zařízení zobrazovaly pouze relevantní úlohy. Chcete-li nastavit filtr, vyberte typ filtru a otevřete seznam hodnot a poté vyberte hodnotu, podle které chcete filtrovat. K dispozici jsou následující filtry:

    - **Výrobní jednotka** – Tento filtr je filtrem nejvyšší úrovně. Obvykle odkazuje na velkou pracovní oblast, která obsahuje několik skupin prostředků a jednotlivé prostředky.
    - **Skupina prostředků** – Tento filtr je filtrem střední úrovně. Obvykle odkazuje na kolekci souvisejících prostředků v omezené oblasti pracovního prostoru. Pokud nejprve vyberete filtr **Výrobní jednotka**, seznam skupin prostředků zobrazí pouze skupiny z této jednotky. Jinak zobrazí všechny dostupné skupiny prostředků.
    - **Prostředek** – Tento filtr je nejkonkrétnějším filtrem. Obvykle odkazuje na konkrétní stroj nebo jiný samostatný prostředek. Pokud nejprve vyberete filtr **Skupina prostředků** nebo **Výrobní jednotka**, seznam prostředků zobrazí pouze prostředky z této skupiny nebo jednotky. Jinak zobrazí všechny dostupné prostředky.

1. Vyberte **OK**.
1. Zobrazí se přihlašovací stránka a vaše zařízení je připraveno k použití.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Povolení pracovníkovi přepsat výchozí filtry

Jednotlivým pracovníkům můžete udělit oprávnění ke změně nastavení filtru na jakémkoli zařízení, které používají. Pro pracovníky, kteří mají toto oprávnění, poskytuje rozhraní pro provádění výrobního provozu tlačítko **Filtr** na stránkách **Všechny úlohy** a **Aktivní úloha**.

> [!NOTE]
> Pokud pracovník změní filtr, použije se od této chvíle nový filtr pro všechny uživatele, kteří se přihlásí k zařízení.

Chcete-li pracovníkovi umožnit přepsat výchozí filtry úloh, které byly pro zařízení nastaveny, postupujte takto.

1. Přejděte na **Čas a docházka \> Nastavení \> Pracovníci registrace času**.
1. Vyberte pracovníka v seznamu, čímž otevřete stránku **Pracovníci registrace času** tohoto pracovníka.
1. Na kartě **Registrace času** nastavte možnost **Nastavit filtry** na *Ano*.

## <a name="run-the-interface-in-full-screen-mode"></a>Spuštění rozhraní v režimu celé obrazovky

Často budete rozhraní pro provádění výrobního provozu spouštět na zařízení používaném výhradně pro tento účel. Proto má smysl spouštět rozhraní v režimu celé obrazovky, aniž by se zobrazovala jakákoli navigace nebo prohlížeč Chrome.

- Chcete-li skrýt navigační podokno zobrazené v Supply Chain Management, přidejte na konec adresy URL v adresním řádku prohlížeče následující text: `\&limitednav=true`.
- Chcete-li také skrýt adresní řádek prohlížeče, použijte nativní režim celé obrazovky prohlížeče. (Pokyny najdete v dokumentaci k prohlížeči.)

Horní část následujícího obrázku ukazuje, jak rozhraní ve výchozím nastavení vypadá. Spodní část ukazuje, jak to vypadá v režimu celé obrazovky, když je skrytý navigační panel.

![Standardní rozhraní vs. rozhraní na celou obrazovku.](media/pfei-full-screen.png "Standardní rozhraní vs. rozhraní na celou obrazovku")

## <a name="extend-the-session-past-12-hours"></a>Prodloužení relace na více než 12 hodin

Ve výchozím nastavení se rozhraní pro provádění výrobního provozu automaticky odhlásí, pokud ho nikdo po dobu 12 hodin nepoužívá. Uživatel Supply Chain Management se poté musí znovu přihlásit. Časový limit však můžete prodloužit až na 90 dní.

Chcete-li prodloužit časový limit, přihlaste se k Supply Chain Management a přejděte na **Správa systému \> Uživatelé \> Rozšíření relace**. Zadejte uživatelský účet Supply Chain Management, který se používá pro přihlášení k zařízení, a počet hodin, po které by relace měla zůstat aktivní.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]