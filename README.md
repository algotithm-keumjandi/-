# 해싱01_신연재

https://school.programmers.co.kr/learn/courses/30/lessons/42576
파이썬 Lv 1 완주하지 못한 선수


def solution(participant, completion):
    hash ={} # 해시 딕셔너리
    for i in participant:
        if i in hash:
            hash[i] += 1
        else:
            hash[i] = 1
    for i in completion:
        if hash[i] == 1: # hash값이 1일 경우 동명이인 없음
            del hash[i]
        else:
            hash[i] -= 1
    answer = list(hash.keys())[0]
    return answer
