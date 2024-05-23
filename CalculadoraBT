(function() {
    function pad(num) {
        return ('00' + num).slice(-2);
    }

    function strToTime(timeStr) {
        var parts = timeStr.split(':');
        return new Date(1970, 0, 1, parts[0], parts[1], parts[2]);
    }

    function calcularRetorno(tempoDuracao, horarioChegada) {
        var duracaoParts = tempoDuracao.split(':');
        var duracaoSeconds = (+duracaoParts[0] * 3600) + (+duracaoParts[1] * 60) + (+duracaoParts[2]);
        
        var chegadaTime = strToTime(horarioChegada);
        
        var retornoTime = new Date(chegadaTime.getTime() + duracaoSeconds * 1000);

        var hours = pad(retornoTime.getHours());
        var minutes = pad(retornoTime.getMinutes());
        var seconds = pad(retornoTime.getSeconds());

        return hours + ':' + minutes + ':' + seconds;
    }

    var tempoDuracao = prompt("Digite o tempo de duração do ataque (HH:MM:SS):");
    var horarioChegada = prompt("Digite o horário de chegada do ataque (HH:MM:SS):");

    var resultadoRetorno = calcularRetorno(tempoDuracao, horarioChegada);

    alert("Horário de retorno do ataque: " + resultadoRetorno);
})();
