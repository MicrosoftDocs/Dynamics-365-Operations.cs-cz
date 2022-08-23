---
title: DPH intrakomunitárního plnění
description: Tento článek uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku.
author: AdamTrukawka
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic
ms.author: atrukawk
ms.search.validFrom: 2019-06-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1dbad270010fecc3b3f2148dd2efd841ef4cd75c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283036"
---
# <a name="intra-community-vat"></a>DPH intrakomunitárního plnění

Tento článek uvádí informace o tom, jak se vypočítává a zaúčtovává daň z přidané hodnoty (DPH) pro Českou republiku.

Když právnické osoby, které mají primární adresu v České republice, nakupují od členských států Evropské unie (EU), měly by provést vlastní vyměření DPH, aby se zajistilo, že jsou splněny následující podmínky:

- DPH na výstupu se platí v období DPH podle data vystavení faktury. (Toto je datum dokumentu.)
- DPH na vstupu nebyla odečtena před přijetím dokumentu. (Toto je datum registru DPH.)

Informace o intrakomunitární DPH mohou být vypočteny a zaúčtovány automaticky. Když zaúčtujete fakturu dodavatele z EU, musí být vytvořeny dvě transakce DPH se stejnou částkou: jedna pro DPH závazku a druhá pro DPH pohledávky. Chcete -li nastavit systém tak, aby vyhovoval tomuto požadavku, postupujte takto.

1. Přejděte do nabídky **Závazky** \> **Nastavení** \> **Parametry závazků**.
2. Na kartě **Hlavní kniha a DPH** na záložce s náhledem **DPH** nastavte možnosti **DPH intrakomunitárního plnění** a **Datum dokladu pro DPH intrakomunitárního plnění** na **Ano**.
3. Vytvořte dva kódy daně z přidané hodnoty: jeden, který má kladné procento daně z přidané hodnoty, a druhý, který má záporné procento daně z přidané hodnoty.
4. Vytvořte skupinu daně z prodeje obsahující kladné i záporné kódy daně z prodeje.
5. Pro záporný kód daně z prodeje vyberte parametr **DPH intrakomunitárního plnění**.
6. V denících vyberte parametr **Datum dokumentu pro intrakomunitární DPH**.

Při zaúčtování nákupní faktury, pohledávka DPH a závazek DPH jsou účtovány ve stejnou dobu. V případě kladných transakcí daně z prodeje je datum registru DPH nastaveno na datum registru DPH ze stránky **zaúčtování faktury** a směrování daně z prodeje závazek. V případě záporných transakcí daně z prodeje je datum registru DPH nastaveno na datum dokumentu a směrování DPH je pohledávka.
